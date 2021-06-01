## Creating tasks
Task is a saved configuration of a database tool. It can be started from the task management view or from the menu by a single click.
You can create tasks for frequently used tools.
Also, tasks can be [[scheduled|Task Scheduler]] for regular execution.

### Create task from tool configuration
You can save the tool configuration into a task and run your task later with a single click.
For example you can start [[Data Transfer]] wizard and configure the data export from several tables in the MySQL database into CSV files:

![](images/ug/tools/task-save-from-tool.png)

Click on the `Save configuration as task` button and fill the task properties:

![](images/ug/tools/task-create-dialog.png)

Now click on the `Open Tasks view` link to open the task list:

![](images/ug/tools/task-view.png)

### Editing/running tasks

From the task view you can add, edit, remove and execute saved tasks.
You can use the context menu or view tools for that:
![](images/ug/tools/task-view-menu.png)

By clicking on `Edit` or by double-clicking on a task you can open the tasks edit wizard. In this wizard you can change the task settings as well as the actual tool configuration. You can change the set of input objects for data transfer or any export a configuration. After changing the task settings, click on the `Update configuration in task` button (it is on the last page of the task configuration wizard).
![](images/ug/tools/task-edit-wizard-objects.png)

### Create task from task management view
You can create a task from scratch using tasks view. Open tasks view and click on the  `Create new task` button in the view toolbar or in the context menu.
In the task wizard you can choose the task category, task type and name. On the next wizard pages, actual tool configuration pages will be shown (they depend on the chosen task type).

### Scheduling tasks

You can schedule tasks for later/regular execution. See the [[Task Scheduler]] article.
