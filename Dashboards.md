**Dashboards** tool allows DBAs and programmers to quickly identify performance, disk space issues, number of connections and other important KPIs associated with a single database connection. To learn more about database connections, see Database Connections. 

By default, DBeaver is delivered with a number of predefined sets of dashboards for such data bases as PostgreSQL, MySQL, Oracle and Exasol. Custom dashboards are also supported. To learn more about custom dashboards, see Creating a New Dashboard section below.

# Managing Dashboards Panel

Dashboard panel is a collection of real-time dashboards, that is dashboards that are continuously updated. 
Dashboards displayed on the dashboard panel are actually a combination of continiously run SQL SELECT queries and charts continiously built on the fetched data.

## Opening Dashboard Panel

To open Dashboard panel click the **Open Dashboard** button  in the main toolbar. The default configuration of the dashboard panel for the current database connection will appear. To learn more about database connections, see Database Connections.

You can also right-click a connection name in the **Database Navigator** editor and select **Open Dashboard** menu option or use keyboard shortcut Ctrl+Alt+Shift+B and the dashboards panel will be opened. 

The following controls are available in the dashboard panel toolbar:

Button| Description
----|-----
Settings|
Add dashboard|
Remove dashboard|
Reset dashboards|

## Adding Dashboards 

To add a dashboard to the Dashboard panel press button **Add dashboard** in the dashboard panel's toolbar and choose one of the dashboards from the list of available dashboards. 

**Note** Different databases have different sets of predefined dashboards. DBeaver is delivered with sets of predefined dashboards for such databases as Postgress SQL, MySQL, Oracle, and Exasol. It is also possible to create new custom dashboards, for more details see Creating New Dashboards.

You can also add a dashboard by right-click in any place of the dashboard panel and then select the **Add dashboard** menu option.

## Removing Dashboards

To remove a dashboard from the Dashboard panel, click on the dashboard you want to remove and press the button **Remove dashboard** in the dashboard panel toolbar  or select **Remove dashboard** option in the dashboard's context menu.

## Resetting Dashboards

If you want to restart data change tracking you can reset dashboards.

You can reset all dashboards displayed in the dashboard panel by a single click on the **Reset dashboards** button in the dashboard panel toolbar.

To reset a particular dashboard right-click on it and select **Reset dashboards** menu option or left click a dashboard and press the **Reset dashboards** button in the dashboard panel toolbar.

## Changing Dashboard Representation

To adjust dashboard representation settings right click on a dashboard and select the **Settings** menu option, and in the opened dialog change the required parameters. 

The following dashboard representation parameters can be adjusted:

Parameter|Description
----|-----
Name|
Description|
Update periods(ms)|
Maximum items|
View|
Show legend|
Show grid|
Show domain axis|
Show range axis|

## Adjusting Dashboard Configuration

To adjust dashboard configuration right-click on a dashboard and select the **Settings** menu option, in the opened dialog box press the **Configuration** button. 

The following dashboard parameters can be configured:

Parameter|Description
----|-----
ID|
Name|
Database|
Data type|
Calc type|
Value type|
Interval|
Fetch type|
Description|
Queries|
Default view|
Update period(ms)|
Maximum items|

**Note** Predefined dashboards are read-only and cannot be re-configured, but you can copy them and use as templates to create new dashboards with any query you want. To learn about creating new dashboards, see Creating New Dashboards section. 

## Printing Dashboards

If you want to print out a screenshot of a dashboard, right-click the dashboard to be printed and select the **Print…** option.

## Detaching Dashboards 

If you have several monitors and would like to place a dashboard into a separate screen, you can either detach the whole dashboard panel or a single dashboard and drag-and-drop it to any place you want.

To detach the whole dashboard panel right click on the dashboard's tab name and select the **Detach**menu option.

To detach a single dashboard make a double left click over it. You can also right click the dashboard and choose the View Dashboard option in the context menu opened.

## Changing Dashboard View

You can change representation of a dashboard and view it as a Pie, Bar or Time series. To change the view of a dashboard, right click on it and select option **View as** menu option and select the view you prefer.

## Saving Dashboards

If you want to save a screenshot of a dashboard locally in PNG format, right click on it and select the **Save as ...** option in the context menu displayed. 
                                                                                                                                                                                                                          
## Copying Dashboards to Clipboard 

To copy a dashboard into the clipboard, right click on the dashboard and use *Copy to Clipboard* menu option.

## Zooming 

For Time series and Bar dashboard representation the following zooming options are available:

* Zoom In
* Zoom Out
* Zoom Reset



