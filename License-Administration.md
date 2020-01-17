**Note: This functionality is available only in [[Enterprise-Edition]].**

### License import

DBeaver EE asks user to import license file if this file cannot be found in the local license storage.
For individual users this is the most simple and convenient way to import product license.
![](images/license-not-found.png)

There are several ways to automate license management process:

#### Put the license file to the predefined locations

On start DBeaver will look for license file in the following locations: 
- Windows
    - `%HOMEPATH%\.dbeaver-ee-license.dat`
    - `%APPDATA%\DBeaverData\workspace6\.metadata\.dbeaver-ee-license.dat`
- Linux

#### Passing license file through [[Command-Line|command line]]

You can add command line parameter `license <license-path>` to the DBeaver EE shortcut.
Also you can add this parameter to `dbeaver.ini` config file.
