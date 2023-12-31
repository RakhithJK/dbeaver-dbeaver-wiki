Panels provide additional space in the [Data editor](Data-Editor) in which you can manipulate data. The panels are handy if you work with complex types (structures, arrays), long text data, or BLOBs. Panels appear as tabs in an additional pane in the right hand side of the Data tab:

![](images/ug/Panels.png)

This additional pane appears only when you open one of the four panels:

* Calc
* Grouping
* Metadata
* Value viewer (default)

To open the panels, click **Panels** on the bottom toolbar. By default, the Value viewer panel opens. Alternatively, you can open the Value panel by pressing <kbd>F7</kbd> on a cell.
To open the other panels, click the down arrow next to the **Panels** button and click the name of the panel on the menu:

![](images/ug/Panels-menu.png)

Panels will also open if you try to inline-edit a cell with a complex data type.

To close the panels, click the **Panels** button again or click the standard Close (cross) icon in the upper right corner of each panel.  
You can also show and hide panels by clicking the **Configure** button (![](images/ug/Configure-columns-visibility-icon.png)) on the bottom toolbar and then **Toggle result panels** on the Configure dropdown menu.

## Value Viewer

The Value viewer panel displays just one value that is currently in focus and allows editing.
 
![](images/ug/Value-Viewer.png)

The toolbar of the Value panel contains the following buttons:

Button|Name|Description
------|----|-----------
![](images/ug/XML_editor_icon.png)|**Content viewer settings**|Opens a menu with a set of options for content view change.
![](images/ug/XML_editor_save_to_file_icon.png)|**Save to file...**|Allows saving the content to a local file. **NOTE**: This button is only available for XML, JSON and Binary content.
![](images/ug/XML_editor_load_from_file_icon.png)|**Load from file...**| Allows uploading data from a local file. **NOTE**: This button is only available for XML,JSON and Binary content.
![](images/ug/Apply-cell-value-button.png)|**Apply cell value**|Displays the data table changes in the Value viewer. **NOTE**: This button does not save changes made to the database. To save the changes in the database, you need to use the **Save** button on the bottom toolbar of the [Data Editor](Data-Editor)..
![](images/ug/Auto-apply-value-button.png)|**Auto-apply value**|Еnables the automatic display of changes made in the Value viewer in the data table. When auto-saving is enabled, the changes appear in the data table at the same time when they are made in the Value viewer.**NOTE**: This button does not save changes made to the database. To save the changes in the database, you need to use the **Save** button on the bottom toolbar of the [Data Editor](Data-Editor).

## Metadata Panel
The Metadata panel displays metadata for each cell in the row containing the cell currently in focus. You can just view the metadata.

![](images/ug/Metadata-panel.png)

## Calc Panel

The Calc panel is useful for getting basic statistics across data in several columns and rows:

![](images/ug/Aggregate-panel.png)

You can select several columns and rows in standard ways - by pressing and holding the left mouse button or by clicking cells while holding the <kbd>Ctrl</kbd> or <kbd>Shift</kbd> keys. The panel updates dynamically to show statistics for the selected data.

To see the data grouped by columns, click the Group by columns button (![](images/ug/Group-by-columns-button.png)). To remove the grouping by columns and see the summary values for all columns, click the same button again.

By default, the panel applies and displays results for two functions – **Count** and **Count Distinct**. To add other functions, click the **Add function** (![](images/ug/Add-function-button.png)) button on the toolbar of the panel or right-click one of the rows in the Aggregate panel and click **Add function** on the context menu and then click the name of the function. The following functions are available:

* Sum
* Average
* Minimum
* Maximum
* Median
* Mode

To remove an individual function, click the function and then click **Remove function** (![](images/ug/Remove-function-button.png)) on the toolbar of the panel, or right-click the function and click **Remove function** on the context menu. To remove all functions, click **Reset** (![](images/ug/Reset-function-button.png)) on the toolbar or on the context menu.

You can copy the value of a particular function to the clipboard - right-click the row and click **Copy Value** on the context menu.  
You can also copy all functions with their values - right-click in the table and click **Copy All** on the context menu. 

## Grouping Panel

The Grouping panel provides tools to calculate statistics based on a table of a custom SQL query.
It uses GROUP BY queries to extract unique values for COUNT (default), SUM, AVG, MIN, MAX and other analytics functions displaying the results in dedicated columns.  
To obtain the grouping results for one or more columns of a data table, open the Grouping panel, then, in the results table, put the cursor onto the data type icon of the table header so that the cursor turns into a hand pointer (![](images/ug/hand-pointer.png)), and drag-n-drop the column(s) into the panel:

![](images/ug/Grouping-drag-n-drop.png)

If you add several columns to the panel, DBeaver groups data in the order in which the columns go and calculates statistics based on the grouping.

![](images/ug/Grouping-Panel.png)

By default, the COUNT function is used. You can add other functions as well. To add a function:

1. Click the **Edit grouping columns** button on the panel`s toolbar.
2. In the Grouping Configuration window, in the **Functions** area, click **Add**, then type the function into the new row:
   * You can use the auto-complete options DBeaver provides.
   * You need to indicate the column name in brackets. COUNT is the only function that supports `*` instead of the column name.
3. Click **OK**:
  
   ![](images/ug/Grouping-new-function.png)

To remove a function, in the same Grouping Configuration window, click the function and click **Remove** and then **OK**. To remove all functions, click **Clear** and then **OK**.

You can also add or remove columns using the same Grouping Configuration window. To add a column:

1. Click the **Edit grouping columns** button on the panel`s toolbar.
2. In the Grouping Configuration window, in the **Columns** area, click **Add**, then type the column name into the new row (you can use auto-complete options DBeaver provides), and then click **OK**:  

   ![](images/ug/Grouping-add-column.png)

For MySQL/MariaDB databases you can also add a column with an expression - the expression will be calculated in the resulting column:

![](images/ug/Grouping-column-expression.png)

To remove a column, in the Grouping Configuration window, in the **Columns** area, click the column name, then **Remove** and **OK**. To remove all columns, click **Clear** and **OK**.  
Another way to remove a column is to click the column and then the **Remove grouping column** button (![](images/ug/Grouping-remove-columns.png)) in the panel`s toolbar. Clicking the **Clear grouping** button (![](images/ug/Clear-columns-button.png)) removes all results from the Grouping panel.

## References panel

The references panel allows you to see all the related information for the chosen row from other connected tables. The information is presented in an additional data viewer window, filtered to show the information related to the currently selected row. If a table opened in data viewer has a foreign key referencing another table, or it is referenced with a foreign key by another table, all of those connected tables can be picked from a dropdown list.

![](images/reference-panel-list.png)

When a table that is referenced by a foreign key in the current table is chosen, the information from the row corresponding to a referenced key will be shown, in this situation the record mode is enabled by default, but it can be turned off like in a normal data viewer.

![](images/references-panel-fk.png)

When a table that references the current table is chosen, the references panel will show all the rows that refer a selected primary key in the current table.

![](images/references_panel-references.png)