**Note: This feature is available in [Lite](Lite-Edition), [Enterprise](Enterprise-Edition), and [Ultimate](Ultimate-Edition) editions only.**

### Manual license import

Commercial versions of DBeaver ask the user to import the license file if they cannot find it locally.
It is the most simple and convenient way to import the product license for individual users.

![](images/license-not-found.png)

### License management automation

There are several ways to automate the license management process. It makes sense for a multi-user environment.

#### Put the license file to the predefined locations

While DBeaver is starting up, it will look for a license file in the following locations: 

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

You can add the command line parameter `license <license-path>` to the DBeaver EE shortcut.
Also, you can add this parameter to the `dbeaver.ini` config file.

[Command line](Command-Line) reference.
