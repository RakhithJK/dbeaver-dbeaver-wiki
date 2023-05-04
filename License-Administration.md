**Note: This feature is available in [Lite](Lite-Edition), [Enterprise](Enterprise-Edition), [Ultimate](Ultimate-Edition) and <a href="https://dbeaver.com/dbeaver-team-edition">Team</a> editions only.**

### Manual license import

Commercial versions of DBeaver ask the user to import the license file if they cannot find it locally.
It is the most simple and convenient way to import the product license for individual users.

![](images/license-not-found.png)

### License management automation

There are several ways to automate the license management process. It makes sense for a multi-user environment.

#### Put the license file to the predefined locations


Add the license .dat file to the following locations: 

- Windows
    - `%HOMEPATH%\.dbeaver-ee-license.dat`
    - `%APPDATA%\DBeaverData\workspace6\.metadata\.dbeaver-ee-license.dat`
- MacOS X
    - `~/.dbeaver-ee-license.dat`
    - `~/Library/DBeaverData/workspace6/.metadata/.dbeaver-ee-license.dat`
- Linux
    - `~/.dbeaver-ee-license.dat`
    - `$XDG_DATA_HOME/DBeaverData/workspace6/.metadata/.dbeaver-ee-license.dat`


**To create the license .dat file you need to download the license .txt file from the DBeaver website and change its file type  to the .dat one.**


**Please follow the next steps:**

1. Install DBeaver
2. Create the license .dat file. It should be named as `.dbeaver-%PRODUCT_PREFIX%-license.dat` (_.dbeaver-ue-license.dat_, _.dbeaver-ee-license.dat_, _.dbeaver-le-license.dat_). The file's location is `%APPDATA%` in the end user home (`C:\Users\Eloise\AppData\Roaming\DBeaverData\workspace6\.metadata\.dbeaver-ue-license.dat`) or `%HOMEPATH%` (`C:\Users\Eloise\.dbeaver-le-license.dat`).
3. Add text from the license .txt file (NOT including headers) to the .dat file.
4. Launch DBeaver from Start Menu




#### Passing license file through command line

You can add the command line parameter `license <license-path>` to the DBeaver EE shortcut.
Also, you can add this parameter to the `dbeaver.ini` config file.

[Command line](Command-Line) reference.
