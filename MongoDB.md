### Overview
DBeaver EE supports MongoDB schema browser, data viewer, SQL and JavaScript queries execution. 
Also it supports various administrative tools (like server sessions manager).  
DBeaver uses MongoDB Java driver 3.8.0 to operate with server. It supports MongoDB servers from 2.x to 4.x.  

### Connecting to MongoDB Server
You can connect directly to a server or use SSH tunneling or SOCKS proxy.  
You can specify server address as host/port/database configuration or you can enter target database URL with all necessary parameters:

![](images/database/mongodb/mongodb-connection-init.png)
![](images/database/mongodb/mongodb-connection-url.png)
![](images/database/mongodb/mongodb-connection-props.png)
![](images/database/mongodb/mongodb-connection-ssh.png)

### Browsing Mongo collections

You can view/edit MongoDB collections content as standard relational tables (grid/plain text presentations) or as JSON documents.  
Presentation can be switched in the Results Viewer toolbar.  
In grid DBeaver will try to unify all documents in some particular collection (as they have the same structure/the same set of properties).  

![](images/database/mongodb/mongodb-data-json.png)

![](images/database/mongodb/mongodb-data-grid.png)

![](images/database/mongodb/mongodb-data-edit.png)

### Executing JavaScript
JS statements can be executed in SQL editor as usual.

Mongo scripting reference

Following example creates a user in the current database.
```js
db.createUser(
  {
    user: "testuser",
    pwd: "test",
    roles: []
  }
)
```

This example returns all documents in collection 'test_col':
```js
db.test_col.find().toArray()
```

Note: script will be executed in the current database.  
You can not set explicit database name in your query.  
Current database can be changed in SQL Editor toolbar or in Database Navigator.  

### Executing SQL
You can use standard SQL statements (SELECT, INSERT, UPDATE, DELETE) to manipulate Mongo data.

```sql
SELECT * FROM test_col 
WHERE propName.subProp='value';

UPDATE FROM test_col 
SET propsName.val1=123
WHERE propName.subProp='value'
```

SELECT queries support WHERE, ORDER BY, GROUP BY and HAVING clauses. 

Nested JSON fields can be divided by dot.
If your field contains any special characters (e.g. spaces, dashes, etc) you must enclose it with double quotes. For example:
```sql
SELECT title FROM movies WHERE info."imdb-details".rating > 6
```

#### Working with dates

If you need to operate with dates then you must specify them in ISO format. It is possible in both Jsava Script and SQL dialects:
```js
db.dates.insert([
	{value: new Date("2016-05-18T16:00:00Z")},
	{value: new Date("2017-05-18T16:00:00Z")},
	{value: new Date("2018-05-18T16:00:00Z")},
	{value: new Date("2019-05-18T16:00:00Z")},
	{value: new Date("2020-05-18T16:00:00Z")}	
])
```

```js
db.dates.find({
	value: { $gte: new Date('2018-05-18T16:00:00Z') }
}).toArray()
```

```sql
SELECT value FROM dates
WHERE value > ISODate('2018-05-18T16:00:00.000Z')
ORDER BY value DESC
```

#### Working with object IDs

When you need to find document by ID you must use function `ObjectId`:

```sql
SELECT * FROM documents
WHERE _id = ObjectId('5f9c458018e3c69d0adc0fbd')
ORDER BY value DESC
```
