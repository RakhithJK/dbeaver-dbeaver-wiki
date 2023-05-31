### Create

1) In the corresponding table, click on the **Foreign Keys** tab, right-click, and select **Create New Foreign Key**
   from the menu.

   ![](images/tutorial_images/11_Create_New_FK.png)

- Additionally, to create a new foreign key, you can utilize the **Create New Foreign Key** button ![](images/tutorial_images/11e_FK_Button.png) located at the bottom of the **[Editor panel](Data-Editor)**.  


2) Choose the Reference table, Unique Key, and hit save.

   ![](images/tutorial_images/11a_FK_parameters.png)

   **Note**: If necessary, set the On Delete and On Update clauses to dictate what happens when you delete or update a row
in the main table.

3) After hitting **OK**, a window displaying the newly created foreign key will appear.

   ![](images/tutorial_images/11b_FK_After_Saving.png)
4) Persist the changes.

### Modify

You can rename a foreign key, add a comment, and tweak the **On Delete** and **On Update** rules. To
view parameters, and double-click the foreign key name.

![](images/tutorial_images/11d_FK_Properties.png)

### Delete

To delete a foreign key, right-click on the key's name in the **[Properties editor](Properties-Editor)** and select
**Delete**, or you can select the necessary column and press the <kbd>Delete</kbd> key.

![](images/tutorial_images/11c_Delete_FK.png)

**Warning**: Be extra cautious here, as deleting a key can significantly affect your data.

### Restrictions

* Referential Integrity: Foreign keys enforce referential integrity. The values in the foreign key column must
  match those in the referenced primary key.
* Impact on Performance: Managing foreign keys can slow down insert and update operations because of the need to check
  referential integrity.
* No Circular References: Circular foreign key references are not permitted in most databases where two or more tables refer to each other.
* Delete and Update Operations: Deleting or updating rows from the referenced table can be complicated because of the
  need to preserve referential integrity.

* Schema Modifications: Changes to the schema of a table (like altering data types or column deletions) can be
  restricted if a foreign key references the table.

**Note**: these limitations can vary based on the specific SQL database system you are using, such as PostgreSQL, MySQL,
Oracle, SQL Server, etc. Always refer to the detailed documentation for your database system.