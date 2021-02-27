Sometimes you need to compare data from two sources (tables) which have almost identical data with just few differences.
There may be a plenty reasons to do so: quickly visualize all the differences and navigate through them by your sight,
to copy differing rows or individual values or export them using [Data Transfer](Data-transfer). 

### Preparing the tool
1. You will need to choose one or two desired tables in the [Database Navigator](Database-Navigator) - it may be the
   tables from the same databases or from different databases or even from different RDBMS (e.g. PostgreSQL and MySQL).
2. Then choose <kbd>Database</kbd> &rArr; <kbd>Compare/Migrate</kbd> &rArr; <kbd>Data Compare</kbd> from the menu and the
   Data Compare Wizard will appear. Here you can preview selected tables or choose other ones. Then you can navigate
   to the second page.
3. After reaching the second page one may wonder about the purpose of it - don't worry, it's not that difficult: you
   should choose columns that will be used as a **unique key** during comparison (the amount of columns must be equal).
   If the _keys_ chosen wrong, it may lead to invalid results. By default, if the table has unique key in it, it will
   be chosen automatically during the initial setup:
   ![](images/ug/tools/data-compare-wizard-constraints.png)
   Without unique keys the rows cannot be compared properly, since there's no way to distinguish between individual rows.
4. After reaching the last page, you can tweak limits (e.g. you only care about `N` first rows) and exclude categories
   of the resulting rows (e.g. you are not interested in modified rows). Also, you can press <kbd>Save task</kbd> button
   save configuration in a [Task](Task-Management) to use it later, or [Schedule](Task-Scheduler) it,
   _although it is not very useful right now, but we have plans to support exporting results as an SQL script and more._ 

### Viewing the results
After finishing the wizard, you can press <kbd>Start</kbd> button to begin actual process of comparison - it may take
some time depending on the databases you're comparing, the amount of data in them, and your network speed (*).

When the results are ready, DBeaver will play _beep_ sound, and the editor will open:
![](images/ug/tools/data-compare-editor.png)
Here you can examine the differences, swap the panels using <kbd>Swap Containers</kbd> button in the toolbar,
or preview summary including statistics by using <kbd>Show Summary</kbd> button in the toolbar too. Everything you can
do in the regular data editor is it possible to perform here - you can copy data or transfer it to other database, except
you cannot modify values.

_* - Please note that the actual preview is only available when Data Compare is launched through the wizard - otherwise only
statistics will be written into the [Task Log](Task-Management#Execution-log)._

### Under the hood
This section is under construction. It will include information about the engine's implementation details and more.