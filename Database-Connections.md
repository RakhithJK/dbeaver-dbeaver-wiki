To be able to manage your database in DBeaver, you need to create a connection to this database – see [Creating Connections](https://github.com/dbeaver/dbeaver/wiki/Connecting-to-Databases). A connection includes a driver and a number of configuration parameters including the location of the database and credentials to access it.  You need to create a separate connection to every database you want to manage. Every database type requires its own set of connection parameters.

Connections reside in the [Database Navigator](https://github.com/dbeaver/dbeaver/wiki/Database-Navigator) and in the [Projects](https://github.com/dbeaver/dbeaver/wiki/Projects) views. In these views, you can:
* Edit connections, see [Editing Connections](https://github.com/dbeaver/dbeaver/wiki/Edit-Connection)
* Rename and delete connections - via corresponding context menu items, see [Database Navigator](https://github.com/dbeaver/dbeaver/wiki/Database-Navigator)
* Connect to and disconnect from databases using connections, see [Connect to Database](https://github.com/dbeaver/dbeaver/wiki/Connect-to-Database) and [Disconnect from Database](https://github.com/dbeaver/dbeaver/wiki/Disconnect-from-Database).

Database connections might have the following states:

  ![](images/ug/PostgreSQL-icon.png) - not connected  
  ![](images/ug/DB-icon-not-connected.png) - has network settings specified (such as SSH tunnel, etc.)   
  ![](images/ug/DB-icon-connected.png) - connected  
  ![](images/ug/Connection-error-icon.png) - connection error  