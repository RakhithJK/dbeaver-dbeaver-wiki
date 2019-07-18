It is possible to install DBeaver in silent mode using Windows Installer command line parameters.  
This might be very useful for mass install automation (SSCM and other similar systems).  
Installer was improved in DBeaver 5.3.3, special thanks to [https://github.com/Drizin/NsisMultiUser](https://github.com/Drizin/NsisMultiUser) team.  

### Parameters 

Command line parameters supported by DBeaver installer:

Parameter|Description
---|---
/S | silent mode, requires /allusers or /currentuser, case-sensitive
/D=path | (installer only) set install directory, must be last parameter, without quotes, case-sensitive
/allusers | (un)install for all users, case-insensitive
/currentuser | (un)install for current user only, case-insensitive
/uninstall | (installer only) run uninstaller, requires /allusers or /currentuser, case-insensitive

In order to install with /allusers parameter current user must have administrator permissions.

### Installer return codes (decimal):

Code|Meaning
---|---
0 | normal execution (no error)
1 | (un)installation aborted by user (Cancel button)
2 | (un)installation aborted by script
666660 | invalid command-line parameters
666661 | elevation is not allowed by defines
666662 | uninstaller detected there's no installed version
666663 | executing uninstaller from the installer failed
666666 | cannot start elevated instance
other | Windows error code when trying to start elevated instance"
