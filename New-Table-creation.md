
### You can create tables, columns, primary keys, and foreign keys using DBeaver. These tools allow you to organize data efficiently and ensure data integrity.
</br></br>

### Tables
1. In the **Database Navigator**, right click the **Tables** and select **Create New Table**. <br/></br>

    ![](images/tutorial_images/1_CreateNewTable.png)</br>

2. In the **Properties**, specify the table name (by default, a new table is created with the name "NewTable"). <br/></br>

    ![](images/tutorial_images/2_NewTable_NoData.png)</br></br>

3. As soon as you set the table name, right-click on the **Column screen**, and select **Create New Column**. <br/></br>

    ![](images/tutorial_images/4_RightClick_CreateNewColumn.png)</br></br>

**Note**: Another way to add a new column is to expand the table view in the **Database Navigator** and **Create New Column** from the context menu.  

![](images/tutorial_images/4a_ExpandTable_CreateNewColumn.png)</br></br>


### Columns
The **Edit Attribute** window (which appears after you click **Create New Column**) allows you to customize the settings of a column in a database table, such as its name, data type, length, not null, auto increment, and default value. <br/></br>
![](images/tutorial_images/5_ColumnEdit.png)</br></br>


### Primary Keys
1. Move to the **Keys** tab of the corresponding table, right-click on the screen, and **Create New Key**.</br></br>

    ![](images/tutorial_images/8_NewConstraint.png)</br></br>


2. Select the column and save. </br></br>

    ![](images/tutorial_images/9_PrimaryKey.png)</br></br>

3. Once you save the changes, a window will appear displaying the newly created **Primary Key**. <br/></br>

    ![](images/tutorial_images/10a_TableAfterSaving.png)</br></br>


3. To **Save the table**, select the desired table in the editor panel and press 'Ctrl+S' (or 'CMD+S' for Mac OS). Then, choose **Persist** to save the changes. <br/></br>

    ![](images/tutorial_images/10_Table_Save.png)</br></br>

**Note**: You can also save changes using **Top menu** -> **File** -> **Save**, **Persist** the changes. </br> Additionally, you can save changes using the **Save** button ![](images/tutorial_images/10b_SaveButton.png) at the bottom of the editor panel.

### Foreign Keys
1. Move to the **Foreign Keys** tab of the corresponding table, right-click on the screen, and **Create New Foreign Key**. <br/></br>
    ![](images/tutorial_images/11_CreateNewForeignKey.png)</br></br>
2. Select the Reference table, Unique Key, and save. <br/></br>
    ![](images/tutorial_images/11a_ForeignKey.png)</br></br>

    **Note**: If needed, specify the desired behavior for when a row is deleted or updated from the main table, using the 'on delete' and 'on update' clauses.</br></br>

3. Save the table.