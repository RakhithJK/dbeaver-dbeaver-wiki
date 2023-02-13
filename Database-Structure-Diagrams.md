You can view a database structure in the standard ERD (Entity Relation Diagram) form. ER diagrams are available for all tables and schemas (databases).  

The ER diagram for a table shows the table itself and its relations with other tables inside the schema. To view the ER diagram for a table or view, double-click the table or view in the [Database Navigator](Database-Navigator) and then, in the [Database Object Editor](Database-Object-Editor), switch to the **ER Diagram** tab:

![](images/ug/ERD-Db-Structure.png)

To view the ER diagram for a full database schema, double-click the schema name in the Database Navigator or the previous node in the path (usually - **Tables**):

![](images/ug/ERD-previous-node.png)

![](images/ug/ERD-DB-Schema.png)

NOTE: Table and schema diagrams are read-only. You can rearrange the layout, drag-n-drop elements inside a diagram but you cannot save the changes state or delete/add anything. This is because the diagrams represent the actual state of databases.

## Relationship Notation

Lines representing the relationship between tables can look different depending on the nature of the relationship. Please note that any line can have only one beginning and one end. We may have links between two tables not only for one pair of attributes, which means that several associations will be displayed:

![image](https://user-images.githubusercontent.com/49681450/199467855-e65fa503-e5cc-47e1-96bc-92556814691a.png)




Notation|Description
---------------|-----------
![image](https://user-images.githubusercontent.com/49681450/199478029-2d466c7d-c445-41be-8ee0-2738c257fa78.png)|A solid line means that the foreign key column in one table is a primary key in another table 
![image](https://user-images.githubusercontent.com/49681450/199477732-a008f182-5b47-41c2-b9e8-a5ab1361fe98.png)|A dashed line means that the foreign key column is not a primary key but a regular column in another table 
![image](https://user-images.githubusercontent.com/49681450/199476816-ed9abb97-0941-42ea-a003-f9fcc5b764e6.png)|A black dot is used as the start of the line 
![image](https://user-images.githubusercontent.com/49681450/199477303-dc5d4c6e-d03a-47df-bfd9-f5f285500b16.png)|A diamond is used at the end of the link when the column in the source table is optional (there is no NOT NULL)



A one-to-one relationship is always a solid line due to the unique primary key - foreign key relationship:

![image](https://user-images.githubusercontent.com/49681450/199478724-26ea5405-ba4d-4409-9802-c89ec01a0295.png)


A dashed line is for the one-to-many relationship:

![image](https://user-images.githubusercontent.com/49681450/199481540-f3d4a8f8-e328-4364-b02f-c46b243e5a80.png)
