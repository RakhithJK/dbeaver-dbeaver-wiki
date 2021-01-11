**Note: This functionality is available only in [[Enterprise Edition]].**

As the name suggests, the _composite task_ is 
[a type of task that consists of other tasks](https://imgur.com/a/jQyU9pJ). Just like the other type of tasks, 
the composite tasks can be scheduled via [task scheduler](Task-Scheduler.md).
Let's take a look at what they can offer.

### Creating a _composite task_

The first thing we need to open _Create a task_ dialog. You can do it in multiple ways:

![](images/comp-task-create-1.gif)
![](images/comp-task-create-2.gif)
![](images/comp-task-create-3.gif)
![](images/comp-task-create-4.gif)
![](images/comp-task-create-5.gif)

Choose _Composite task_, enter the task name, description (optional), and hit _Next_.

You will be presented with the following dialog:

![](images/comp-task-settings-dialog.png)

### Setting up a _composite task_

When creating a composite task you need to specify which tasks the composite task consists of.

This can be done:

1. By adding an existed task:

![](images/comp-task-add-existing.gif)

2. By creating a new task and adding it simultaneously:

![](images/comp-task-add-new.gif)

3. By drag-and-dropping a task from the _Database tasks panel_:

![](images/comp-task-add-dnd.gif)

As a side note, you can add a composite task to your new composite task.

You can edit tasks in the same dialog, 
delete a task from a composite task, change the execution order: 

![](images/comp-task-edit.gif)

There is also a very important checkbox, _Ignore task error_. 
The tasks from the _composite task_ are executed in the order they appear in the settings dialog. 
Executing a task from a _composite task_ might produce an error that will block next tasks 
from proceeding. The _Ignore task error_ checkbox can be used to bypass this behaviour.