**Note: This functionality is available only in [[Enterprise-Edition]].**

DBeaver can schedule task execution for regular executions.
In version 6.x DBeaver supports only native Windows Task Scheduler. You can configure scheduler (CRON) manually on other OSes by calling `dbeaver-cli` command line tool (see below).

### Scheduling tasks from the Tasks view
You can open the tasks view from the main toolbar:

![](images/ug/tools/task-main-toolbar.png)

or from the main menu `Window`.
Select a task that you want to schedule in the tasks view and open the context menu:

![](images/ug/tools/task-schedule-menu.png)

Scheduler configuration dialog will be opened. You can configure task frequency, recurrence period and start time there:

![](images/ug/tools/task-schedule-settings.png)
![](images/ug/tools/task-schedule-settings-monthly.png)

Then click on a `Schedule` button. If everything is configured correctly you will see the confirmation dialog:

![](images/ug/tools/task-schedule-success.png)

If anything goes wrong you will see an error message dialog. Error details can be viewed in the [[Error Log|Log-files]] view.

You can change scheduler settings at any moment by choosing `Edit scheduled task` command from the context menu. You can also cancel scheduling by clicking on `Remove schedule`.

### See schedule details and logs in the Windows Task Scheduler

You can see and change scheduled task details in the Windows Task Scheduler. Click on the `Open scheduler settings` command in the task view context menu:

![](images/ug/tools/task-schedule-windows-task-manager.png)

All DBeaver tasks are located in a folder `DBeaver`.

### Monitoring task execution

You can look through the task execution logs in the right side of the tasks view. By double clicking on a task run item you can see the full log with all details/errors/warnings:

![](images/ug/tools/task-run-logs.png)

DBeaver keeps the task run logs in the [[workspace|Workspace Location]] directory, subfolder `.metadata/task-stats`.

### Running tasks from the command line

The task scheduler uses the DBeaver [[command line|Command-Line]] interface to perform task execution. Command line parameter `-runTask TASK_ID` launches saved task execution (immediately).  
`TASK_ID` has form `@projectName:taskName`. You can omit project name part if you have only one project in your workspace.
Use `dbeaver-cli` executable to run tasks.  
Draw your attention that if you use `dbeaver` executable (by any reason) you will need to add command line parameter `-nosplash` to avoid splash screen appearance.

### Configuring CRON scheduler

`TBD`