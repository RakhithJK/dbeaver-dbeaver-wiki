**Note: This functionality is available only in [[Enterprise-Edition]].**

### License import

By default DBeaver will ask user to import license file if it won't find it in local license storage.
There are several ways to automate this process:

#### Predefined license file locations

On start DBeaver will look for license file in the following locations: (Windows)
- `%HOMEPATH%\.dbeaver-ee-license.dat`
- `%APPDATA%\DBeaverData\workspace6\.metadata\.dbeaver-ee-license.dat`

#### Passing license file thru [[Command-Line|command line]]

You can add command line parameter `license <license-path>` in the DBeaver EE shortcut.
Also you can add this parameter in `dbeaver.ini` config file.
