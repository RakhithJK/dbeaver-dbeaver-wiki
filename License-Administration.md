**Note: This functionality is available only in [Enterprise Edition](Enterprise-Edition).**

### Manual license import

DBeaver EE asks user to import license file if this file cannot be found in the local license storage.
For individual users this is the most simple and convenient way to import product license.

![](images/license-not-found.png)

### License management automation

There are several ways to automate license management process. It makes sense for multi-user environment.

#### Put the license file to the predefined locations

On start DBeaver will look for license file in the following locations: 

- Windows
    - `%HOMEPATH%\.dbeaver-ee-license.dat`
    - `%APPDATA%\DBeaverData\workspace6\.metadata\.dbeaver-ee-license.dat`
- MacOS X
    - `~/.dbeaver-ee-license.dat`
    - `~/Library/DBeaverData/workspace6/.metadata/.dbeaver-ee-license.dat`
- Linux
    - `~/.dbeaver-ee-license.dat`
    - `$XDG_DATA_HOME/DBeaverData/workspace6/.metadata/.dbeaver-ee-license.dat`


#### Passing license file through command line

You can add command line parameter `license <license-path>` to the DBeaver EE shortcut.
Also you can add this parameter to `dbeaver.ini` config file.

[Command line](Command-Line) reference.