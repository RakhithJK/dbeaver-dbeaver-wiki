**Note: This functionality is available only in [[Enterprise-Edition]].**

DBeaver can schedule task execution for later regular execution.
In version 6.x DBeaver supports only native Windows Task Scheduler. On other OSes you can configure scheduler (CRON) manually by calling `dbeaver-cli` command line tool (see below).

### Scheduling tasks from Tasks view
You can open tasks view from main toolbar:

![](images/ug/tools/task-main-toolbar.png)

or from main menu `Window`.
In tasks view select a task you want to schedule and open context menu:

![](images/ug/tools/task-schedule-menu.png)

Scheduler configuration dialog will open. You can configure task frequency, recurrence period and start time:

![](images/ug/tools/task-schedule-settings.png)
![](images/ug/tools/task-schedule-settings-monthly.png)

Then click on `Schedule` button. If everything was configured correctly then you will see confirmation dialog:

![](images/ug/tools/task-schedule-success.png)

If anything will fo wrong you will see error message dialog. Error details can be viewed in [[Error Log|Log-files]] view.

You can change scheduler settings at any moment by choosing `Edit scheduled task` command from context menu. You can also cancel scheduling by clicking on `Remove schedule`.

### See schedule details/logs in Windows Task Scheduler

You can see/change scheduled task details in Windows Task Scheduler. In task view context menu click on `Open scheduler settings` command:

![](images/ug/tools/task-schedule-windows-task-manager.png)

All DBeaver tasks are located in folder `DBeaver`.

### Monitoring task execution

You can see task execution logs in the right side of tasks view. By double clicking on task run item you can see full log with all details/errors/warnings:

![](images/ug/tools/task-run-logs.png)

DBeaver keeps task run logs in [[workspace|Workspace Location]] directory, subfolder `.metadata/task-stats`.

### Running tasks from command line

Task scheduler uses DBeaver [[command line|Command-Line]] interface to perform task execution. Command line parameter `-runTask TASK_ID` launches saved task execution (immediately).  
`TASK_ID` has form `@projectName:taskName`. You can omit project name part if you have only one project in your workspace.
Use `dbeaver-cli` executable to run tasks.  
If you will use `dbeaver` executable (by any reason) then you need to add command line parameter `-nosplash` to avoid splash screen appearance.

### Configuring CRON scheduler

`TBD`