**Query Builder** is a user-friendly visualization tool that will help you make sense of your complex database designs. It can be useful when you need to understand the various relationships between different tables. Also, it can be helpful for those who is not much familiar with SQL scripting or if you don't want to insert script commands manually. The tool creates SQL scripts automatically based on visual schema you create. 

**To open Visual Query Builder:**
1. In the [SQL Editor](https://github.com/dbeaver/dbeaver/wiki/SQL-Editor) tool bar click the **Open Query Builder** button. The **Query Builder** will be opened on the right.

 **To visualize table connections:**
1. Open **Visual Quiery Builder**. 
2. Drug and drop  tables from the **Database Navigator** pane into the **Visual Query Builder** field. All the connections existing between the tables will be shown automatically.

**To create a connection between the tables:**
1. Drag and drop  tables from **Database Navigator** pane into the **Visual Query Builder** field. 
2. Press the left mouse button when the cursor is over the column of one table, holding the right mouse button pressed drag the cursor to the column of another table and release the right mouse button. The connection between the selected columns of the tables will be created visually and in the SQL script a new join will be added. 

**To remove a connection between the tables:**
1. To remove a connection between the tables click on it. The connection will be highlighted.
2. Press Delete or use select **Delete** option in the context menu. The visual connection will be removed and the corresponding join will be automatically removed from the SQL script.

**To build a query:**

1. To define query data source in **Visual Query Builder** you need to aselect columns from the selected tables. To select a column click the check-box next to its name and the column will be added to the **Columns** tab of the **Query Settings Editor** and SQL SELECT query will be created automatically in the script field.
2. In the **Visual Query Builder** vertical toolbar **Execute SQL statement** button to get the results in the same tab or **Execute SQL statement in new tab** button to get the results in a new tab.

**To open Query Setting Editor:**
1. In the **Visual Query Builder** vertical toolbar press **Visual query builder settings** button and  the **Query Settings Editor** tab will appear below.

**To edit query settings:**
The following query settings can be adjusted:

| Setting Name | Description |
-----------|-------------|
| **Columns** | **Alias** - set a user-friendly name of the column to be displayed in the **Results** tab.  The change will be immediately displayed in the SQL script.You can also add and remove columns in this editor. To add a column use the **Add** button on the right - a new instance will be added to the table. Click on the first cell and select a column name from the list of available columns.To remove the column, click on the row containing its name and press the **Remove** button       on the right.To change the display order of columns in the result table use Move up and Move down buttons on the right. |
| **Conditions** | To add a new expression use the **Add**  button on the right - a new instance will be added to the table. To remove an expression, click on the row containing the expression and press  the **Remove** button on the right. **Left Operand** - defines the left operand of the conditional expression. Click the cell in the **Left Operand** column and a drop down list of all available  columns will be displayed. Select a column you want to use as the left operand in your conditional expression. **Operation** - defines the comparison rule between the left and the right operands of the conditional expression. To set a comparison rule click the cell in the **Operation** column and select the rule you need from the drop down list appeared.The condition where will be automatically added to the SQL script. |
| **Joins** | Joins cannot be  added or removed by means of **Query Settings Editor**, however, the following join settings can be adjusted here: **Type** - defines the type of the join. Click the cell in the **Type** column - a drop down with available join types will be displayed. Select the required option  from the list by clicking on it.**Alias** - defines a user friendly name of the join. To define this setting click on the cell in **Alias** column and input the name. |
| **Sorting** | Sorting allows to change the order of rows in the result table. To add a new sorting condition use the **Add**  button on the right.To remove a condition use the **Remove** button       on the right. Once a new condition is added, click the first cell in **Conditions or Expressions** column and a drop down list of all available columns will appear. Select the required column by clicking on its name. In **Order** column you can define whether the rows should be sorted in ascending or descending order in the result table. To set the order, click the cell in **Order** column and select the required option from.The order by command will be added to the script. |
| **Miscellaneous** | It is possible to autosave on SQL-editor switch by selecting the **Autosave on SQL-editor switch check-box.** |
