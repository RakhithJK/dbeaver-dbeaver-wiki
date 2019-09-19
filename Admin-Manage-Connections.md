This guide describes how to manage/secure DBeaver database connections.
It is designed for System administrators. Regular users should check [this](Connect-to-database) guide.

### Provide predefined connections
DBeaver keeps connections information in project folder. By default all projects reside in [[workspace|Workspace-Location]].  
Default project folder is [[workspace|Workspace-Location]]\workspace6\General.  

#### DBeaver 6.1.3+
DBeaver keeps information about project connections in file `.dbeaver/data-sources.json`.  
All secured information (user name, password, secret keys, etc) is stored in the encrypted file `.dbeaver/credentials-config.json`.  

DBeaver can load multiple connection files. Any files in project folder matching `.dbeaver/data-sources*.json` pattern will be loaded on startup. So you can create a file, say, `.dbeaver/data-sources-2.json` in the project folder and DBeaver will see it.

#### DBeaver < 6.1.3
DBeaver keeps information about project connections in file `dbeaver-data-sources.xml`. 

DBeaver can load multiple connection files. Any files in project folder matching `.dbeaver-data-sources*.xml` pattern will be loaded on startup. So you can create a file, say, `.dbeaver-data-sources-2.xml` in the project folder and DBeaver will see it.

### Importing connections from CSV/XML
You can import connection from CSV or XML files.

CSV file must have a header row (first line of file) with column names (see list of supported columns below).
XML file should contain top-level element and a set of nested elements. Connections config must be specified in attributes of nested elements. Attribute names are the same as CSV column names.

#### Supported names:
| Name | Meaning |
-----------|-------------|
|name|Connection name|
|url|JDBC URL|
|host|Database server host name|
|port|Database server port|
|database|Database/schema name|
|user|User name|
|password|User password|
You can specify just URL or set host/port/etc setting.  
User name/password are options.

#### Sample CSV
```
name,host,port,server,database,url,user,password,type
Postgre Import XML 1,localhost,5432,,postgres,jdbc:postgresql://localhost:5432/postgres,postgres,postgres,dev
Postgre Import XML 2,localhost,5432,,postgres2,jdbc:postgresql://localhost:5432/postgres2,postgres2,postgres2,prod
```
#### Sample XML
```xml
<connections>
	<connection name="Postgre Import XML 1" host="localhost" port="5432" server="" database="postgres" url="jdbc:postgresql://localhost:5432/postgres" user="postgres" password="postgres" type="dev"/>
	<connection name="Postgre Import XML 2" host="localhost" port="5432" server="" database="postgres" url="jdbc:postgresql://localhost:5432/postgres2" user="postgres2" password="postgres2" type="prod"/>
</connections>
```

### Secure connections from editing
It is possible to make connection settings read-only (protected by password)
- Generate MD5 hash of your password. You can do it from command line using Linux utility md5sum (`md5sum <<<"your password"`) or you can do it online - just google "MD5 hash online".
- Add field`lockPassword` in connection descriptor (in `.dbeaver/data-sources.json` in `connections` element. So it will look like this:

```json
postgres-jdbc-161537836e8-3e0957d039995715": {
   "provider": "postgresql",
   "driver": "postgres-jdbc",
   "name": "PostgreSQL - postgres",
   "save-password": true,
   "show-system-objects": true,
   "read-only": false,
   "folder": "PG",
   "lockPassword": "2ba81a47c5512d9e23c435c1f29373cb"
...
}
```

- Now if user will try to change connection settings he/she will be asked for password
