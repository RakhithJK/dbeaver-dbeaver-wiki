In [Database Navigator](../Database-Navigator) and [Database Object Editor](../Database-Object-Editor) you can filter database objects to include or exclude some of them from the view. You can filter schemas, tables, views and procedures. A dots sign `(...)` next to the node`s name indicates that a filter is applied to its sub-nodes:
![](images/ug/Filtered-object.png)

There are several ways in which you can filter objects.
One of the ways is to filter objects by names of tables and views using the filter field above the tree of objects:

![](images/ug/DB-Nav-filter.png)

To filter objects by the name of a table and view, type the name in the field. The tree dynamically updates to show tables / views with that name. To reset the filter, click the Clear icon  (![](images/ug/Clear-filter-icon.png)) on the right end of the field.

Another way to filter objects is to use the **Filter** item on the context menu of a single object. To filter objects using the **Filter** menu, right-click the object, then click **Filter** on the context menu, and then click one of the items on the submenu:

Filter submenu item|Description
-------------------|-----------
**Hide ‘[object name]’**|Hides the current object while displaying the other ones
**Show only ‘[object name]’**|Shows the current object while hiding the other ones
**Toggle filter**|Inverts the filtering – shows hidden objects and vice versa
**Clear filter**|Removes the filtering to display all objects
**Configure [objects] filter**|Appears only for folder or parent nodes of  database objects - like ‘Tables’, ‘Indexes’, etc. Allows creating a complex filter with multiple filtering criteria, see [Configure Filters](../Configure-Filters).

A third way of filtering is to use the **Filter** item on the context menu on several objects:
1. Select several objects of the same type using Ctrl or Shift keys.
2. Right-click the selection, then click **Filter**, and then choose one of the options on the submenu:

Filter submenu item|Description
-------------------|-----------
**Hide N objects**|Hides the selected objects while displaying the rest
**Show only selected objects**|Shows the selected objects while hiding the rest

To reset such filters, right-click the parent (folder) node displaying the dots sign `(...)`, and then click **Filter -> Clear filter**.
