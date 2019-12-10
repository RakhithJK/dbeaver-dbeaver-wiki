## Database Backup/restore

DBeaver supports native database backup/restore functions for following databases:
  - PostgreSQL
  - MySQL

Native backup restore differs from standard DBeaver [data transfer](Data-Transfer) feature. It uses database native dump formats and it may work much faster as it uses special utilities for direct high-performance database access.

These functions can be accessed from context menu Tools or main menu Database->Tools.
![](images/ug/tools/tools-menu.png)

### Native client configuration
In order to execute native backup/restore tools you need to configure database native client. Native client is a set of binaries (different for different OSes) which will be executed by DBeaver to process actual backup/restore.
Native client configuration can be done in [driver editor dialog](Database-drivers) or directly from backup/restore wizard. Just click on `Client ...` button in the button bar:
![](images/ug/tools/native-client-select.png)  

To configure new client location choose `Browse ...` item and ad new client in the following dialog:  

![](images/ug/tools/native-client-manager.png)

### Database dump object selector
You can choose what schemas/tables you want to backup/dump:
![](images/ug/tools/dump-database-objects.png)

### Database native tool configuration
You can pass a set of additional dump/restore parameters to the native tool. Particular set of configuration options depends on a database type.  
![](images/ug/tools/dump-database-settings.png)