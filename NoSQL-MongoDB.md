**Note: MongoDB extension is available only in [Enterprise Edition](Enterprise-Edition) version.**

### Browsing Mongo collections
You can view/edit Mongo collections content as standard relational tables (grid/plain text presentations) or as JSON documents.  
Presentation can be switched in the Results Viewer toolbar.  
In grid DBeaver will try to unify all documents in some particular collection (as they have the same structure/the same set of properties).

### Executing JS
JS statements can be executed in SQL editor as usual.  
[Mongo scripting reference](https://docs.mongodb.com/v3.0/administration/scripting/)  
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
Note: script will be executed in the current database. You can not set explicit database name in your query.
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
Nested JSON properties can be divided by dot.