# Prerequisites for Debugging
In order to implement interactive debugging of PL/SQL procedures on a Postgres server you need to use plugin_debugger. Plugin_debugger is a typical interactive debugger delivered as an extension and requiring a  shared library preload in Postgres to operate the shared_preload_libraries parameter in settings. The debugger is developed and maintained by the community. Its source code is available for examination and improvement.
 
The debugger provides the required server API for debugging PL/SQL procedures with:

* Breakpoint management;
* Step-by-step tracing;
* Variable acquisition and management.

Installation
------------

As the first step, you need to install the **plugin_debugger** extension in your PostgreSQL database. It is free and open source. You can download the source code [here](https://git.postgresql.org/gitweb/?p=pldebugger.git;a=tree). And you can find the installation README file [here](https://git.postgresql.org/gitweb/?p=pldebugger.git;a=blob_plain;f=README.pldebugger;hb=HEAD).

To install the debugger plugin:

1. Copy this directory to **contrib/** in your PostgreSQL source tree.
2. Run **make; make install**.
3. Edit your **postgresql.conf** file and modify the **shared_preload_libraries** config option to look like the following: **shared_preload_libraries = '$libdir/plugin_debugger'**.
5. Restart PostgreSQL for the new setting to take effect.
6. Run the following command in the database or databases that you wish to debug functions in:  
   **CREATE EXTENSION pldbgapi;**  
  NOTE: On server versions older than 9.1, instead of running the command, you need to run the **pldbgapi--1.0.sql** script directly using psql.

If you use binary builds from pgdg, you can use repository for your Linux distribution. For more information, please see [Official Postgres page] (https://www.postgresql.org/download/).

After installing the plugin on the database server, you need to install the debug plugin from either a marketplace or P2 repository, see this [article](../Optional-extensions) for more information.

You can find a detailed DBeaverCE Debug plugin installation guide from Jkiss P2 repository [here](../DebugPluginInstall).

# How to start debug with local breakpoint
For local breakpoints, stop will be done only for server process launched by the initiator. All other processes will run procedure/function as usual. When you create or run a previously defined debugging session in DBeaver with local breakpoint, the following steps take place:

1. DBeaver creates initiator session and local breakpoint.
2. DBeaver runs procedure\function (with parameters specified) selected for debugging in the initiator session. 
3. The server process reaches breakpoint and displays NOTICE to initiator, in which the PORT is reported for PLDBGBREAK:XX debugging. Then the process opens the socket and becomes blocked, waiting for PROXY connection. If Debug Client cannot get PORT name from the process being debugged, an error message appears.
4. Debug Client creates a session, then tries to establish connection with the debugged process, using PORT from step 3 provided by the initiator. The connection is established via API call **attach_to_port**. If the connection cannot be established, the **Error rcv port number** message appears.
5. PROXY receives PORT from the client, then establishes connection to the process, and returns the session identifier to the client. After that, using the identificator, one can:
   * Send debugging commands to the process;
   * Receive responses from the process;
   * Translate responses to the client.

![](images/debug-local.png|Debug with local breakpoint)

# How to start debug with global breakpoint
Whenever the breakpoint is global, stop will be done for any server process launched by anyone. No modifications or additional calls from the debugged process are required. When you create a session with a global breakpoint, the following steps take place:

1. The client creates a session and then establishes a connection with PROXY (receiving session). After that, the client creates a global breakpoint  for the selected function, and then becomes blocked via the **pldbg_wait_for_target** API call waiting for the server process.
2. PROXY receives the global control point from the client and adds global control point to the shared memory, if the point of this type has not been added before.
3. The initiator creates a connection and runs the selected procedure.
4. On each executed line, the target process checks if the global breakpoint with corresponding conditions exists, and becomes blocked if the breakpoint exists and conditions are met.
5. The target process establishes a connection with PROXY and reports that the breakpoint is reached.
6. Afterwards, the process becomes blocked and waits for PROXY (client) commands. The process will be implementing commands unless the procedure finishes or an exception is thrown. 

![](images/debug-global.png)

Running debugger in DBeaver interface
------------
If you have successfully installed the debugger plugin, and the plugin is up and running, you can start Debug from procedure source page by right-clicking the procedure source text - a context menu appears:

![](images/start-debug.PNG)

You need to choose the type of your debug session: Local or Global.

For a **Global** session, you need to specify the target process PID filter (enter **-1** value for any process): 
![](images/start-debug-global.PNG)

After running a Global session, you need to wait for any (or specified PID) process to call your procedure.

For a **Local** session, you need to specify the executable SQL sentence for starting the target process: 
![](images/start-debug-local.PNG)

In the script editor window, you can see the **select get_count(?)** text that is just a specification of how DBeaver must call your function(procedure) for debug. 

DBeaver is not intended to know about the values of the variables in the procedure being debugged. You need to set the values for call arguments BEFORE you start debugging. 
Your settings might look as follows:  
![](images/start-debug-local-params.png)

If you run debugging now, DBeaver creates a separate connection to the database server, tries to execute the given SQL sentence **select get_count(‘pg_class’)** in this connection, and attaches the debug session to the running SQL context.

After successfully attaching to the target server process, the platform prompts you to switch to the debug perspective:

![](images/debug-perspective.PNG)

After you click **OK**, the debug toolset (perspective) opens:
  
![](images/debug-perspective-win.png)
