The SQL Assist feature provides auto-completion of database object names and SQL commands and other keywords in queries.
 
To perform some object name auto-complete, press <kbd>Ctrl+Space</kbd> or right-click the required place in the query and click **SQL Assist** on the context menu. DBeaver searches for objects in a database, by their names and/or descriptions. 

![](images/ug/SQL-Assist.png)

When you start typing an SQL keyword in a statement, DBeaver offers auto-complete options as well.  
Another auto-complete function is search for completion only within already entered identifiers - press <kbd>Ctrl+Shift+Space</kbd>.  


You can also press <kbd>Ctrl+Space</kbd> after the asterisk in the query like "SELECT * FROM tableName" or like "INSERT INTO tableName (*)" (brackets are important) (you can use ()[]{} brackets) - the asterisk will be replaced with a list of all the table columns.  