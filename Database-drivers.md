You can use pre-configured database driver or create new driver.

DBeaver has a lot of pre-configured driver including SQL, NoSQL, key-value databases, graph databases, search engines, etc.
But sometimes you need to connect to a database which was not configured in DBeaver yet.

All you need is JDBC driver of your database the ret is easy.

### Obtaining JDBC driver

JDBC driver is a program (in Java) which can connect and operate with some local or remote database server. It usually provides all needed functionality to cover 100% of database functionality. Usually JDBC driver are made by database vendors to let customers ability to work with their databases.

JDBC driver consists of one or multiple `jar` files. Jar file is a library which contains program code and some other files.
You need to download driver's jar files before adding them in DBeaver. Sometimes jar files are included in database server distribution - in that case you need to refer your database documentation or ask your DBA.

### Adding driver configuration in DBeaver

#### Open driver manager dialog

You can open driver manager from main menu:  
![](images/ug/drivers/database-menu.png)  
or from Database Navigator view drop-down menu.  
![](images/ug/drivers/driver-manager.png)

#### Add new driver

Just click button New and create new driver.
On driver edit dialog you need to enter all needed information:

![](images/ug/drivers/driver-edit.png)

##### Main parameters

Parameter|Description
----|-----
Driver Name|Name of your driver. It may be any name you like.
Driver Type|Driver provider. In 99% cases you will need Generic driver (JDBC provider)
Class Name|JDBC driver class name. You can get it from documentation or find it jar files (see "Find Class" button description).
URL Template|Template of driver URL. You can leave it empty but in this case you will need to set JDBC URL for each your connection. It is better to define a valid template, this will greatly simplify connections create. See "URL Templates" for detailed description.
Default Port|Default database port. You can get it from documentation or leave it empty.
Embedded|Enable it for server-less databases. This flag affects a few config options related to network/connections management
No Authentication|This means that driver doesn't require authentication (no user/password fields will be shown).
Category|Driver category, deprecated
ID|Driver unique ID, ignore it
Description|Driver description, it is shown on some dialogs/wizards as a hint.

##### Libraries

This is the list of jar files, binary libraries (dll or so) and any other files needed by driver. In most cases you need only jar files.  
Click "Add File" to add single jar file, "Add Folder" to add folder with Java classes/resources and "Add Artifact" to add Maven artifact (see below).  

After you add jar files you can search for all JDBC driver classes which present in these jars. Just click on "Find Class" button and DBeaver will show all of them. In most cases there is just one driver class in driver. If there are many of them then you need to refer to driver's documentation.

##### Maven artifacts

DBeaver can download driver jars directly from Maven repository (it is a global public repository of Java libraries, usually open-source). If your database driver is published on some public repository you can use this feature. Maven artifacts are better than plain jar files because you can see all existing driver versions and can change driver version in runtime without any driver properties reconfiguration.

##### Advanced settings

For most driver you don't need to change any advanced properties.
But in some cases you can use this as a driver tuning (for better performance or for structure fixing).

![](images/ug/drivers/driver-properties.png)

Parameter|Description
----|-----
Driver Name|Name of your driver. It may be any name you like.
