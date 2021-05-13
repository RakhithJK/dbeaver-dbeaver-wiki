### Error Log view

There is an Error Log view (main menu Window->Show View->Error Log) which contains all errors which occurred during the DBeaver runtime.  
You can double click on warning/error in the log viewer and see the error stacktrace. Please attach it to the bug report.  
Also, you can open the full log (all error messages) if you need:  

![](images/error-log-export.png)

### Log files

DBeaver writes different log files. Most of them are Eclipse logs.  
Log files usually reside in the [[workspace|Workspace-Location]]/workspace6/.metadata .  

- On Windows open Explorer and paste path `%APPDATA%\DBeaverData\workspace6\.metadata`.  
- On Linux just type `cd $XDG_DATA_HOME/DBeaverData/workspace6/.metadata`
- On MacOS open path `~/Library/DBeaverData/workspace6/.metadata` in Finder.
  - To view hidden folders press <kbd>Cmd+Shift+.</kbd> in the folder view.

Two standard log files:
- [[workspace|Workspace-Location]]/workspace6/.metadata/.log - all warnings and errors which happen during normal work
- [[workspace|Workspace-Location]]/workspace6/.metadata/dbeaver-debug.log - the same as `.log` plus debug information

In special cases log files can be written in other directories. A special case is an emergency situation when DBeaver cannot start and there is no workspace.
Two typical places to find emergency logs:

- `<install-path>/configuration`
- `${HOME}/.eclipse/org.jkiss.dbeaver.product_<dbeaver-version>`

If you are reporting about some error please attach logs (not the complete file but the valuable part of it).  
Logs are very useful, big number of errors cannot be reproduced/fixed without full error stacktrace.

### Java fatal logs

In rare cases the DBeaver process dies and does not leave any valuable logs. This is caused by a Java VM crash.  
JVM creates a fatal log file for each crash (log gile `hs_err_PID.log`). This log usually resides in the same directory where the DBeaver launcher is (e.g. dbeaver.exe).  
But in some cases it is a write-protected directory and the log file will be created in other folder.  
Instructions on how to find the Java fatal log file: https://docs.oracle.com/javase/9/troubleshoot/fatal-error-log.htm