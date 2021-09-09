# Command line parameters

Command line parameters might be passed directly to dbeaver[.exe] executable.  
In Windows you can also use `dbeaver-cli.exe` executable (it does not spawn a new window so you can see the output messages).  

Also, you can add parameters in the `dbeaver.ini` configuration file - in the beginning of the file and each parameter on its own line.

## DBeaver control
Name|Value|Example
----|-----|-------
-help|Prints help message|
-stop|Quits DBeaver|
-dump|Prints DBeaver thread dump|
-f|Opens file in DBeaver UI|`-f c:\some-path\some-file.sql`
-con|Opens database connection in DBeaver UI|See [connection parameters table](#connection-parameters)
-closeTabs|Closes all open editor tabs|
-disconnectAll|Closes all open connections|
-reuseWorkspace|Force reuse of single workspace by multiple DBeaver instances|
-newInstance|Force new DBeaver instance creation (do not try to reuse already running one)|
-var <img src="images/commercial_big.png" align="top" vspace="4" height="16"/>|Custom variables for runTask. You can change existing variables in the task. You cannot add new task variables with this parameter. You can add several parameters at once to the command line, each starting with "-var". Used right before -runTask. Template: "-var variableName=variableValue"|`-var film=sakila.film`<br/>`-var actor=sakila.actor`<br/>`-runTask "exportFromSakila"`<br/>EE version only.
-runTask <img src="images/commercial_big.png" align="top" vspace="4" height="16"/>|Executes specified task|`-runTask "@projectName:taskName"`.<br/>EE version only. See [[task scheduler]].
-license <img src="images/commercial_big.png" align="top" vspace="4" height="16"/>|Path to the EE license file|`-license "/etc/licenses/dbeaver.txt"`.<br/>EE version only.


## System parameters

Name|Value|Example
----|-----|-------
-nl|Locale|en_US
-data|Workspace path|c:\ProgramData\MyWorkspace
-nosplash|Omits splash screen|true
-clean|Clears all Eclipse caches. Use it if DBeaver fails to start after a version upgrade.
-vmargs|VM parameters|See [VM arguments table](#vm-arguments)

### VM arguments

You can pass any advanced Java parameters supported by your local JVM (Oracle, OpenJDK, IBM, etc).  
Parameters supported by Oracle JVM (11): https://docs.oracle.com/en/java/javase/11/tools/java.html

Parameters supported by all JVMs:

Name|Value|Example
----|-----|-------
-Xms|Sets initial memory available for DBeaver|`-Xmx1000m`
-Xmx|Sets maximum memory available for DBeaver|`-Xmx4000m`

### Connection parameters
All connection parameters must be supplied as a single command line argument, parameters are divided by pipe (`|`). Parameter name and value are divided by `=`.  
Example: -con "driver=sqlite|database=C:\db\SQLite\Chinook.db|name=SQLiteChin|openConsole=true|folder=SQLite"

Name|Value|Example
----|-----|-------
name|Connection name|`Test connection`
driver|Driver name or ID|`driver=sqlite`, `driver=mysql`, etc
url|Connection URL. Optional (JDBC URL may be constructed by driver from other parameters)|`url=jdbc:sqlite:C:\db\SQLite\Chinook.db`
host|Database host name (optional)|`host=localhost`
port|Database port number (optional)|`port=1534`
server|Database server name (optional)|`server=myserver`
database|Database name or path (optional)|`database=db-name`
user|User name (optional)|`user=root`
password|User password (optional)|`password=mysecret`
auth|Authentication model ID. See [Auth models](Database-authentication-models) |`auth=postgres_pgpass`
authProp.propName|Custom authentication parameters (depends on driver and [auth model](Database-authentication-models))|`authProp.oracle.net.wallet_location=C:/temp/ora-wallet`
savePassword|Do not ask user for a password on connection|`savePassword=true`
showSystemObjects|Show/hide system schemas, tables ,etc|`showSystemObjects=true`
showUtilityObjects|Show/hide utility schemas, tables ,etc|`showUtilityObjects=true`
folder|Put new connection in a folder|`folder=FolderName`
autoCommit|Sets connection auto commit flag (default value depends on driver)|`autoCommit=true`
prop.propName|Advanced connection parameters (depend on driver)|`prop.connectTimeout=30`
id|Connection id|`oracle_thin-16a88e815bd-70598e648cedd28c` (useful in conjunction with `create=false`)
connect|Connect to this database|`connect=false`
openConsole|Open SQL console for this database (sets `connect` to true)|`openConsole=true`
create|Create new connection|`create=false` (true by default). If set to false then an existing connection configuration will be used. The name or id parameter must be specified.
