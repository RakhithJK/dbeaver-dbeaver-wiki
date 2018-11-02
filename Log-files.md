There is Error Log view (main menu Window->Show View->Error Log) which contains all errors occurred during DBeaver runtime.  

DBeaver writes different log files. Most of them are Eclipse logs.  
Usually log files reside in the workspace.  
Default workspace location is in the user home subfolder `.dbeaver4`. (`${HOME}/.dbeaver4`). On Windows you usually can find it in `C:\Users\YourName\.dbeaver4`.  

Two standard log files:
- `<workspace-path>/.metadata/.log` - all warnings and errors which happens during normal work
- `<workspace-path>/.metadata/dbeaver-debug.log` - the same as `.log` plus debug information

In special cases log files can be written in other directories. Special case is an emergency situation when DBeaver can't start and there is no workspace.
Two typical places to find emergency logs:

- `<install-path>/configuration`
- `${HOME}/.eclipse/org.jkiss.dbeaver.product_<dbeaver-version>`

If you are reporting about some error please attach logs (not complete file but valuable part of it).  
Logs are very useful, big number of errors can't be reproduced/fixed without full error stacktrace.