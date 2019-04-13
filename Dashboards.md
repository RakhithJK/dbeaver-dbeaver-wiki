**Dashboards** tool allows DBAs and programmers to quickly identify performance, disk space issues, number of connections and other important KPIs associated with a single database connection. To learn more about database connections, see [Database Connections](https://github.com/dbeaver/dbeaver/wiki/Database-Connections). 

By default, DBeaver is delivered with a number of predefined sets of dashboards for such data bases as PostgreSQL, MySQL, Oracle and Exasol. Custom dashboards are also supported. To learn more about custom dashboards, see Managing Dashboards section below.

# Managing Dashboards Panel

Dashboards panel is a collection of real-time dashboards, that is dashboards that are continuously updated. 
Dashboards displayed on the dashboards panel are actually a combination of continiously run SQL SELECT queries and charts continiously built on the data fetched.

## Opening Dashboard Panel

To open dashboards panel click the **Open Dashboard** button ![](images/ug/dashboards/Open_Dashboard_icon.png) in the main toolbar. The default configuration of the dashboards panel for the current database connection will appear. To learn more about database connections, see [Database Connections](https://github.com/dbeaver/dbeaver/wiki/Database-Connections).

You can also right-click a connection name in the **Database Navigator** editor and select **Open Dashboard** menu option or use keyboard shortcut <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>B</kbd> and the dashboards panel will be opened. 

![](images/ug/dashboards/Open_Dashboard_Menu_Option.png)

The following controls are available in the dashboards panel toolbar:

Icon|Name|Description
----|-----|-----
![](images/ug/dashboards/Dashboard_Settings_icon.png)|**Settings**|Allows managing dashboards' configuration.
![](images/ug/dashboards/Dashboard_Add_icon.png)|**Add dashboard**| Allows to add dashboards to the dashboard panel.
![](images/ug/dashboards/Dashboard_Remove_icon.png)|**Remove dashboard**| Allows to remove dashboards from the dashboard panel.
![](images/ug/dashboards/Dashboard_Reset_icon.png)|**Reset dashboards**| Allows to restart dashboard calculation.

## Adding Dashboards 

To add a dashboard to the dashboards panel, press the **Add dashboard** button ![](images/ug/dashboards/Dashboard_Add_icon.png) in the dashboards panel's toolbar, choose one of the dashboards from the list of available dashboards and press the **Add** button. 

![](images/ug/dashboards/Adding_dashboard_By_Toolbar_Btn.png)

**Note:** Different databases have different sets of predefined dashboards. DBeaver is delivered with sets of predefined dashboards for such databases as Postgress SQL, MySQL, Oracle, and Exasol. It is also possible to create new custom dashboards, for more details see Managing Dashboards.

You can also add a dashboard by right-click in any place of the dashboards panel and then select the **Add dashboard** menu option.

![](images/ug/dashboards/Adding_dashboard_By_Menu_Optn.png)

## Removing Dashboards

To remove a dashboard from the dashboards panel, click on the dashboard you want to remove and press the button **Remove dashboard** ![](images/ug/dashboards/Dashboard_Remove_icon.png) in the dashboards panel toolbar or select **Remove dashboard** option in the dashboard's context menu.

![](images/ug/dashboards/context_menu_Remove.png)

## Resetting Dashboards

If you want to restart dashboard's calculation you can reset it.

You can reset all the dashboards displayed in the dashboards panel by a single click on the **Reset dashboards** ![](images/ug/dashboards/Dashboard_Reset_icon.png)  button in the dashboard panel's toolbar.

To reset a particular dashboard right-click on it and select **Reset dashboards** menu option or left click a dashboard and press the **Reset dashboards** button in the dashboards panel's toolbar.

![](images/ug/dashboards/context_menu_Reset.png)

## Changing Dashboard Representation

To adjust dashboard representation settings right click on a dashboard and select the **Settings** menu option, then, in the opened dialog change the parameters you want. 

![](images/ug/dashboards/RepresentationSettings_DialogBox.png)

The following dashboard representation parameters can be adjusted:

Parameter|Description
----|-----
**Name**|Defines a name of a dashboard.
**Description**| Defines dashboard's description. Use this field to make it easy to understand what kind of information the dashboard represents.
**Update periods(ms)**| Defines how often dashboard's rendering should be updated. The default value is 1000 ms. 
**Maximum items**|Defines maximum number of fetched items. The default value is 300.
**View**| Defines visual representation of the dashboard. The following options are available: Bar, Pie, Time series.
**Show legend**| If this check-box is selected, the legend will be displayed on the dashboard.
**Show grid**| If this check-box is selected, the grid will be displayed on the dashboard.
**Show domain axis**| If this check-box is selected, the domain axis will be displayed on the dashboard. 
**Show range axis**|If this check-box is selected, the range axis will be displayed on the dashboard. 

## Adjusting Dashboard Configuration

To adjust dashboard's configuration settings right-click on a dashboard, select the **Settings** menu option, then, in the opened dialog box press the **Configuration** menu option. 

![](images/ug/dashboards/ConfigurationSettings_DialogBox.png)

The following dashboard parameters can be configured:

Parameter|Description
----|-----
**ID**| Defines dashboard's ID. Make sure that ID has numeric values in it.
**Name**|Defines dasboard's name.
**Database**|Defines the database driver. To learn moe about database drivers, see [Database Drivers](https://github.com/dbeaver/dbeaver/wiki/Database-drivers).
**Data type**|Defines the data type. The following options are availabe: timerseries (the default option) and statistics. Select timeseries type if you want to track the actual value returned by the server. Select statistics type if your dashboard will show historical data.
**Calc type**|Defines how the data should be calculated. The following options are available: value (the default option) and delta. Select value if you're interested in the current value. Select delta if you want to track the difference between the current value and the previous one. This may be very useful when you work with statistics data, for example.
**Value type**|Defines the value to be shown on the range domain. The following options are available: decimal (the default option), integer, percent, bytes. Choose the value type in accordance with your data, for example, memory usage is convinient to be tracked in KBytes.
**Interval**|Defines time interval to be shown on the domain axis. The following time intervals are available: millicecond(the default option), second, minute, hour, day, week, month, year.
**Fetch type**|Defines whether the query should fetch data from rows or columns.
**Description**| Defines the description of a dashboard. Use this field to make it easy to understand what kind of information the dashboard represents.
**Queries**|Defines an SQL query whose fetched data will be used to build the chart displayed on the dashboard.
**Default view**|Defines the default visual representation of a dashboard on the dashboard panel. The following options are available: Bar, Pie, Time series(the default option).
**Update period(ms)**|Defines how often the dashboard's rendering should be updated.
**Maximum items**| Defines maximum number of items to be fetched for the dashboard.

**Note:** Predefined dashboards are read-only and cannot be re-configured, but you can copy them and use as templates to create new dashboards with any query and other settings. To learn about creating new dashboards, see Managing Dashboards section. 

## Setting Connection Prefereces

By default, if there is no active connection to the database and you open its dashboards panel, all the dashboards on the panel will be empty.

You can force database connection on the dashboard panel's activation by pressing the **Settings** button ![](images/ug/dashboards/Dashboard_Settings_icon.png) on the dashboards panel's toolbar and then selecting the **Connect on activation** check-box.


## Detaching Dashboards 

If you have several monitors and would like to place a dashboard into a separate screen, you can either detach the whole dashboards panel or a single dashboard and drag-and-drop them to any place you want.

To detach the whole dashboard panel right click on the dashboard's tab name and select the **Detach**menu option.

![](images/ug/dashboards/context_menu_Detach.png) 

To detach a single dashboard make a double left click over it. You can also right click the dashboard and then, select the **View Dashboard** menu option, the dashboard will be detached from the panel and you will be able to move it to any place of your screen.

![](images/ug/dashboards/context_menu_View_dashboard.png) 

## Changing Dashboard View

You can change the representation of a dashboard and view it as a Pie, Bar or Time series. To change the view of a dashboard, right click on it and select **View as** menu option.

![](images/ug/dashboards/context_menu_View_as.png) 

## Copying Dashboards to Clipboard 

To copy a dashboard into the clipboard, right click on the dashboard and use **Copy to Clipboard** menu option, the screenshot of the dashboard will be placed to the clipboard.

![](images/ug/dashboards/context_menu_Copy_to_clipboard.png)

## Saving Dashboards

If you want to save a screenshot of a dashboard locally in PNG format, right click on it and select the **Save as ...** option in the context menu displayed. 

![](images/ug/dashboards/context_menu_Save_as.png)

## Printing Dashboards

If you want to print out a screenshot of a dashboard, right-click the dashboard to be printed and select the **Print…** option.

![](images/ug/dashboards/context_menu_Print.png)
                                                                                                                                                                                                                          
## Zooming 

For Time series and Bar dashboard representations the following zooming options are available in the dashboard's context menu:

* Zoom In
* Zoom Out
* Zoom Reset

![](images/ug/dashboards/context_menu_Zoom.png)

# Managing Dashboards 

## Creating Dashboards

You can create a new custom dashboard either from scratch or from already existing dashboards. 

### To create a dashboard from scratch:

1. Press the **Settings** button ![](images/ug/dashboards/Dashboard_Settings_icon.png) in the dashboards panel toolbar.
2. In the opened dialog box click **Manage...** button.
3. In the **Manage dashboards** window click **New dashboard...** button.
4. Set up all configurational parameters as required and press **OK**. To learn more about dashboard's configuration parameters, see  [Adjusting Dashboard Configuration](https://github.com/dbeaver/dbeaver/wiki/Dashboards#adjusting-dashboard-configuration).

![](images/ug/dashboards/New_dashboard_from_scratch.png)

### To create a dashboard from template:

1. Press the **Settings** button ![](images/ug/dashboards/Dashboard_Settings_icon.png) in the dashboards panel toolbar.
2. In the opened dialog box click **Manage...** button.
3. In the **Manage dashboards** window select any of the existing dashboards from the list and click **Copy**.
4. Adjust all configurational parameters as required and press **OK**. To learn more about dashboard's configuration parameters, see  [Adjusting Dashboard Configuration](https://github.com/dbeaver/dbeaver/wiki/Dashboards#adjusting-dashboard-configuration).

![](images/ug/dashboards/New_dashboard_from_template.png)

## Editing Dashboards

If you need to change dashboard's name , ID or any other configurational setting, you can edit a dashboard.
**Note:** Only custom dashboards can be edited, predefined dashboards are read-only, but you can use them as templates and create a custom dashboard whose parameters will be editable. To learn how to create dashboards from templates, see [Creating Dashboards](https://github.com/dbeaver/dbeaver/wiki/Dashboards#creating-dashboards).

### To edit dashboard's configuration:

1. Press the **Settings** button ![](images/ug/dashboards/Dashboard_Settings_icon.png) in the dashboards panel toolbar.
2. In the opened dialog box click **Manage...** button.
3. In the **Manage dashboards** window select any of the custom dashboards from the list and click **Edit...**.
4. Adjust all configurational parameters as required and press **OK**. To learn more about dashboard's configuration parameters, see  [Adjusting Dashboard Configuration](https://github.com/dbeaver/dbeaver/wiki/Dashboards#adjusting-dashboard-configuration).

![](images/ug/dashboards/Editting_dashboard.png)

## Deleting Dashboards

**Note** Predefined dashboards cannot be deleted, but any of the custom dashboards can be deleted. 

If you want to delete a dashboard, follow the steps described below.

### To delete a dashboard:

1. Press the **Settings** button ![](images/ug/dashboards/Dashboard_Settings_icon.png) in the dashboards panel toolbar.
2. In the opened dialog box click **Manage...** dashboards.
3. In the **Manage dashboards** window select any of the custom dashboards from the list and click **Delete**.

![](images/ug/dashboards/Deleting_dashboard.png)
