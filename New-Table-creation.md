
You can create tables, columns, primary keys, and foreign keys using DBeaver. These tools allow you to organize data efficiently and ensure data integrity.  


## Tables
1. In the **Database Navigator**, select the necessary database, right-click on **Tables** and choose **Create New Table**.  

   ![](images/tutorial_images/1_CreateNewTable.png)</br>

2. In the **Properties**, specify the table name (by default, a new table is created with the name "NewTable").  

   ![](images/tutorial_images/2_NewTable_NoData.png)</br></br>

3. As soon as you set the table name, right-click on the **Column screen**, and select **Create New Column**.  

   ![](images/tutorial_images/4_RightClick_CreateNewColumn.png)</br></br>

   **Note**: Another way to add a new column is to expand the table view in the **Database Navigator** and **Create New Column** from the context menu.  

   ![](images/tutorial_images/4a_ExpandTable_CreateNewColumn.png)  


## Columns
1. Click on **Create New Column**.
2. In the **Edit Attribute** window, customize the settings of a column. Adjust the settings as needed, including the **Name**, **Data type**, **Length**, **Not null**, **Auto increment**, and **Default** value of the column.

   ![](images/tutorial_images/5_ColumnEdit.png)  

## Primary Keys
1. Move to the **Keys** tab of the corresponding table, right-click on the screen, and **Create New Key**.  

   ![](images/tutorial_images/8_NewConstraint.png)  


2. Select the column and save.  

   ![](images/tutorial_images/9_PrimaryKey.png)  

3. Once you save the changes, a window will appear displaying the newly created **Primary Key**.  

   ![](images/tutorial_images/10a_TableAfterSaving.png)  


4. To **Save the table**, select the desired table in the editor panel and press **Ctrl+S** (or **CMD+S** for Mac OS). Then, choose **Persist** to save the changes.  

   ![](images/tutorial_images/10_Table_Save.png)

   **Note**: You can also save changes using **Top menu** -> **File** -> **Save**, **Persist** the changes. Additionally, you can save changes using the **Save** button ![](images/tutorial_images/10b_SaveButton.png) at the bottom of the editor panel.

## Foreign Keys
1. In the corresponding table, click the **Foreign Keys** tab, right-click on the screen, and **Create New Foreign Key**.  
  
   ![](images/tutorial_images/11_CreateNewForeignKey.png)  

2. Select the **Reference table**, **Unique Key**, and save.  

   ![](images/tutorial_images/11a_ForeignKey.png)  

   **Note**: If needed, specify the desired behavior for when a row is deleted or updated from the main table, using the 'on delete' and 'on update' clauses.

3. Save the table.