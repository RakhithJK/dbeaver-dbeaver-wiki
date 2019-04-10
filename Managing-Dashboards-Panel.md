**Dashboard Panel** tool allows DBAs and programmers to quickly identify performance, disk space issues, number of connections and other important KPIs associated with a single database connection. To learn more about database connections, see Database Connections. 

Dashboards displayed on the dashboard panel are actually a combination of SQL SELECT scripts being run on a regular basis and charts being built on the data SQL script is extracting.

By default, DBeaver provides a number of predefined sets of dashboards for such data bases as PostgreSQL, MySQL, Oracle and Exasol. You can also create custom dashboards for one of these drivers. To learn more about custom dashboards, see Creating a New Dashboard section below.

## Opening Dashboard Panel

To open Dashboard panel click the **Open Dashboard** button  in the main toolbar. The default configuration of the dashboard panel for the current database connection will appear. To learn more about database connections, see Database Connections.

You can also right-click a connection name in the **Database Navigator** editor and select **Open Dashboard** menu option or use keyboard shortcut Ctrl+Alt+Shift+B. 


## Viewing Dashboard Configuration

To understand the SELECT script behind a particular dashboard, click a dashboard to select it and press the **Settings** button in the dashboard panel toolbar. 

In the opened dialog press the **Manage...** button  and, in the opened dialog box, find a predefined dashboard, double click it - the dashboard configuration will be opened. 

**Note:** Predefined dashboards cannot be edited, but can be copied and used as templates for creating new dashboards.

## Adding Dashboards

To add a dashboard to the Dashboard panel press button **Add dashboard** in the dashboard panel's toolbar and choose one of the dashboards from the list of available dashboards. 

**Note** Different databases have different sets of predefined dashboards. DBeaver is delivered with sets of predefined dashboards for such databases as Postgress SQL, MySQL, Oracle, and Exasol. It is also possible to create new custom dashboards, for more details see Creating a New Dashboard.

You can also add a dashboard by right-click in any place of the Dashboard panel and then click  the **Add dashboard** menu option.

## Removing Dashboards

To remove a dashboard from the Dashboard panel, click on the dashboard you want to remove and press the button **Remove dashboard** in the dashboard panel toolbar  or select **Remove dashboard** option in the dashboard's context menu.

## Resetting Dashboards

If you want to restart data change tracking you can reset dashboards.

You can reset all dashboards displayed in the dashboard panel by a single click on the **Reset dashboards** button in the dashboard panel toolbar.

To reset a particular dashboard right-click on it and select **Reset dashboards** menu option or left click a dashboard and press the **Reset dashboards** button in the dashboard panel toolbar.

## Printing Dashboards

If you want to print out a screenshot of a dashboard, right-click the dashboard to be printed and select the **Print…** option.

## Detaching Dashboards 

If you have several monitors and would like to place a dashboard into a separate screen, you can either detach the whole dashboard panel or a single dashboard and drag-and-drop it to any place you want.

To detach the whole Dashboard panel right click on the Dashboard's tab name and select the Detach option.

To detach a single dashboard make a double left click over it. You can also right click the dashboard and choose the View Dashboard option in the context menu opened.

## Saving Dashboards

If you want to save a screenshot of a dashboard locally in PNG format, right click on it and select the Save As option in the context menu displayed. 
                                                                                                                                                                                                                          
## Copying Dashboards to Clipboard 

To copy a dashboard into the clipboard, right click on the dashboard and use *Copy to Clipboard* menu option.
