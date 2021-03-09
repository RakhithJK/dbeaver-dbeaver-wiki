## Grid vs. Plain Text Views

You can switch between two data presentations in SE version and four presentations in EE version. Pressing <kbd>CTRL+~</kbd> switches available presentations in turn.
* To see the data in a grid view, similar to an Excel spreadsheet, click the **Grid** button (![](images/ug/Grid-button.png)) on the bottom toolbar of the editor.
* To switch to the plain text view, click **Text** (![](images/ug/Text-button.png)) on the bottom toolbar.
* To switch to JSON view (available in EE version only for MongoDB documents and JSON tables), click **JSON** on the toolbar.
* To switch to XML view (available in EE version only for XML tables), click **XML** on the toolbar.

## Table vs. Record Views

The table view is a standard table (Excel-like) in which columns are vertical and rows are horizontal. This view is the default one. If you click the **Record** button in the bottom toolbar of the editor (![](images/ug/Record-button.png)), or press <kbd>Tab</kbd>, or right-click a cell and then click **Layout -> Record** on the context menu, the rows and columns switch positions – columns appear as rows, and rows hide in one **Value** column which now shows only one row of data, and column headers shift from the top of the table to its left side:    
![](images/ug/Record-view.png)  
The Record view is useful if the table contains a big number of columns. To navigate from row to row of data, use the navigation buttons on the bottom toolbar of the editor: ![](images/ug/Navigation-buttons.png)

To return back to the standard table view, click the **Record** button again.

## Rows Coloring
In the data editor, you can color all rows that have the same value as a particular cell of a certain column. To do so, right-click the cell and click **View/Format -> Set row color for {column name = value}** on the context menu:

![](images/ug/Color_rows.png)

Then choose the color in the palette window that appears and click **OK**. The current row and all other rows that contain the same value change their color to the one you selected:

![](images/ug/Colored_rows.png)

To remove the coloring by a particular column, right-click the cell again and click **View/Format -> Clear color for {column name = value}** on the context menu.

## Coloring by Data Types
Besides coloring rows by a value, you can colorize values in columns by data types. To do so, right-click any cell in the table and, on the context menu, click **View/Format -> Colorize Data Types**. Values in cells are colored in different colors according to preferences currently set:

![](images/ug/Colored-Data-Types.png)

You can change the color preferences in the Preferences window: click **Window -> Preferences** on the main menu. Then, in the window, in the navigation pane on the left, expand **User Interface** and then **Appearance**, and then click **Colors and Fonts**:

![](images/ug/Color-Preferences.png)

To remove coloring by data types, on the context menu, click **View/Format -> Colorize Data Types** again.

## Transforming Data Presentation
For string and numeric data types, DBeaver provides tools to transform the data presentation into a number of formats, such as URL and Binary for strings and Epoch Time, Number Radix, etc. for numbers. To change the data presentation in a certain column, right-click a cell in the column, then, on the context menu, click **View/Format -> Set {column name} format** and then click the presentation type name:

![](images/ug/View-as.png)

The Transformer settings window opens showing the value in the chosen format. Click **OK** to apply the change:

![](images/ug/Transformer-settings-window.png)

The values in the column appear in the new format.  
NOTE: For URL format, the resulting cell provides a link to the URL in a browser window. 

To roll back the changes to the default format, right-click any cell in the column, and on the context menu, click **View/Format -> View as -> Default**.

## Structurizing Complex Data Types
For complex data types (that themselves represent a structure), such as objects, structures and arrays, DBeaver provides a tool for breaking them into columns:

![](images/ug/Structurize.png)

To do so, right-click a cell in the column and, on the context menu, click **View/Format -> Visualize complex columns**.

## Configuring Numeric and Time Data Formats
You can specify the exact format of Time, Timestamp, Date, and Number data used in the currently open database or globally. To specify a format, right-click any cell in the table and, on the context menu, click **View/Format -> Data formats**. The Properties window opens displaying the **Data Formats** page:

![](images/ug/Data-format-properties.png)

To configure the format for the current database only, select the **Datasource "[Connection name]" settings** checkbox. To configure the settings globally, to all databases that you have in DBeaver, click **Global settings**.  
You can specify the locale for the data format in the **Locale** area, then, in the **Type** dropdown list, click the name of the data type and then, in the **Settings** table, click the required format.  
To apply the changes and make them visible in the table, click **Apply and Close** and then refresh the window (<kbd>F5</kbd>).
