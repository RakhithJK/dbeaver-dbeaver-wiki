Command line parameters can be passed directly to the DBeaver executable. The way to do this depends on your operating system:

### Windows:
You can use the `dbeaver-cli.exe [parameters]` executable. This executable does not spawn a new window, so you can see the output messages.

### Mac:
Parameters can be passed to DBeaver in one of two ways:

- Use the open command followed by the `-a` flag and the name of the application, along with any necessary arguments. Depending on the version of DBeaver, you might need to specify `DBeaver.app`, `DBeaverEE.app`, `DBeaverLite.app`, or `DBeaverUltimate.app`. For example: `open -a "DBeaver.app" --args [parameters]`. <br>**Note**: This method does not display output messages.
- Pass parameters directly to the DBeaver executable in the terminal using the path where the `.app` file is located. For example: `/Application/Dbeaver.app/Content/MacOS/dbeaver [parameters]`. This method does not spawn a new window, so you can see the output messages.

<br><br>
For both Windows and Mac, parameters can also be added in the `dbeaver.ini` configuration file. These should be written at the beginning of the file, with each parameter on its own line.

# Command line parameters

## DBeaver control
Name|Value|Example
----|-----|-------
-help|Prints help message|
-stop|Quits DBeaver|
-dump|Prints DBeaver thread dump|
-f|Opens the file in DBeaver UI, if the command has -con argument, connects it to datasource|`-f c:\some-path\some-file.sql`
-con|Opens database connection in DBeaver UI|See [connection parameters table](#connection-parameters)
-closeTabs|Closes all open editor tabs|
-disconnectAll|Closes all open connections|
-reuseWorkspace|Forces reuse of single workspace by multiple DBeaver instances|
-newInstance|Forces new DBeaver instance creation (do not try to reuse already running one)|
-bringToFront|Brings the DBeaver window on top of other applications|
-var <img src="images/commercial_big.png" align="top" vspace="4" height="16"/>|Customs variables for runTask. You can change existing variables in the task. You cannot add new task variables with this parameter. You can add several parameters at once to the command line, each starting with "-var". Used right before -runTask. Template: `-var variableName=variableValue`|`-var film=sakila.film`<br/>`-var actor=sakila.actor`<br/>`-runTask "exportFromSakila"`<br/>EE version only.
-vars|Path to a property file with variables|`-vars c:\path\to\file.properties`<br>For more information see [the main article](Admin-Variables#declare-external-variables-in-a-file)
-runTask <img src="images/commercial_big.png" align="top" vspace="4" height="16"/>|Executes specified task|`-runTask "@projectName:taskName"`.<br/>EE version only. See [[task scheduler]].
-license <img src="images/commercial_big.png" align="top" vspace="4" height="16"/>|Path to the EE license file|`-license "/etc/licenses/dbeaver.txt"`.<br/>EE version only.


## System parameters

Name|Value|Example
----|-----|-------
-nl|Locale|en_US
-data|Workspace path|c:\ProgramData\MyWorkspace
-nosplash|Omits splash screen|true
-clean|Clears all Eclipse caches. Use it if DBeaver fails to start after it upgrades.
-vmargs|VM parameters|See [VM arguments table](#vm-arguments)

### VM arguments

You can pass any advanced Java parameters supported by your local JVM (Oracle, OpenJDK, IBM, etc).  
Parameters supported by Oracle JVM (11): `https://docs.oracle.com/en/java/javase/11/tools/java.html`

Parameters supported by all JVMs:

Name|Value|Example
----|-----|-------
-Xms|Sets initial memory available for DBeaver|`-Xmx1000m`
-Xmx|Sets maximum memory available for DBeaver|`-Xmx4000m`

### Connection parameters
All connection parameters must be supplied as a single command line argument. The parameters are divided by pipe (`|`). The parameter name and value is divided by `=`.  
Example: `-con "driver=sqlite|database=C:\db\SQLite\Chinook.db|name=SQLiteChin|openConsole=true|folder=SQLite"`

Name|Description|Example
----|-----|-------
name|Connection name|`Test connection`
driver|Driver name or ID|`driver=sqlite`, `driver=mysql`, etc
url|Connection URL. Optional (JDBC URL may be constructed by a driver from other parameters)|`url=jdbc:sqlite:C:\db\SQLite\Chinook.db`
host|Database host name (optional)|`host=localhost`
port|Database port number (optional)|`port=1534`
server|Database server name (optional)|`server=myserver`
database|Database name or path (optional)|`database=db-name`
user|User name (optional)|`user=root`
password|User password (optional)|`password=mysecret`
auth|Authentication model ID. See [Auth models](Database-authentication-models) |`auth=postgres_pgpass`
authProp.propName|Custom authentication parameters (depends on the driver and [auth model](Database-authentication-models))|`authProp.oracle.net.wallet_location=C:/temp/ora-wallet`
savePassword|Does not ask user for a password on connection|`savePassword=true`
showSystemObjects|Shows/Hides system schemas, tables ,etc|`showSystemObjects=true`
showUtilityObjects|Shows/Hides utility schemas, tables ,etc|`showUtilityObjects=true`
folder|Puts a new connection in a folder|`folder=FolderName`
autoCommit|Sets connection auto commit flag (default value depends on driver)|`autoCommit=true`
prop.propName|Advanced connection parameters (depend on driver)|`prop.connectTimeout=30`
id|Connection id|`oracle_thin-16a88e815bd-70598e648cedd28c` (useful in conjunction with `create=false`)
connect|Connects to this database|`connect=false`
openConsole|Opens the SQL console for this database (sets `connect` to true)|`openConsole=true`
create|Creates new connection|`create=false` (true by default). If it is set as false, then an existing connection configuration will be used. The name or id parameter must be specified.
save|Saves new connection|When `create=true`, then `save=false` (default) makes new connection temporary, `save=true` means that new connection will be saved and accessible between DBeaver launches.

## Declare external variables in a file
See the [main article](Admin-Variables#declare-external-variables-in-a-file)