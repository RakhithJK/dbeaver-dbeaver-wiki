### Error Log view

There is an Error Log view (main menu Window->Show View->Error Log) which contains all errors which occur during the DBeaver runtime.  
You can double click on the warning/error in the log viewer and see the error stacktrace. Please attach it to the bug report.  
Also, you can open the full log (all error messages) if you need:  

![](images/error-log-export.png)

### Log files

DBeaver writes different log files. Most of them are Eclipse logs.  
Log files usually reside in the [[workspace|Workspace-Location]]/workspace6/.metadata .  

- In Windows open Explorer and paste path `%APPDATA%\DBeaverData\workspace6\.metadata`.  
- In Linux just type `cd $XDG_DATA_HOME/DBeaverData/workspace6/.metadata`
- In MacOS open path `~/Library/DBeaverData/workspace6/.metadata` in Finder.
  - To view hidden folders press <kbd>Cmd+Shift+.</kbd> in the folder view.

Two standard log files:
- [[workspace|Workspace-Location]]/workspace6/.metadata/.log - all warnings and errors which happen during normal work
- [[workspace|Workspace-Location]]/workspace6/.metadata/dbeaver-debug.log - the same as `.log` plus debug information

In special cases log files can be written in other directories. A special case is an emergency situation when DBeaver cannot start and there is no workspace.
Two typical places to find emergency logs:

- `<install-path>/configuration`
- `${HOME}/.eclipse/org.jkiss.dbeaver.product_<dbeaver-version>`

If you are reporting an error, please attach the applicable part of the log - not the complete file.  
Logs are very useful. Many errors cannot be reproduced and fixed without a full error stacktrace (all the details).

### Java fatal logs

On the rare occasion that the DBeaver process dies, it does not leave any valuable logs. This is caused by a Java VM crash.  
JVM creates a fatal log file for each crash (log gile `hs_err_PID.log`). This log usually resides in the same directory where the DBeaver launcher is (e.g. dbeaver.exe).  
But in some cases it is a write-protected directory and the log file will be created in other folder.  
Instructions on how to find the Java fatal log file: https://docs.oracle.com/javase/9/troubleshoot/fatal-error-log.htm

### Log files for Team Edition

Log files usually reside in the [[workspace|Workspace-Location]]/team-workspace/.metadata . 

- In Windows open Explorer and paste path `%APPDATA%\DBeaverData\team-workspace\.metadata`.  
- In Linux just type `cd $XDG_DATA_HOME/DBeaverData/team-workspace/.metadata`
- In MacOS open path `~/Library/DBeaverData/team-workspace/.metadata` in Finder.
  - To view hidden folders press <kbd>Cmd+Shift+.</kbd> in the folder view.