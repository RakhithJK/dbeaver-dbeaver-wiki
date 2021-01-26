The installation process depends on the distribution type and your Operational System.

### Windows / MacOS Installer
The installer distribution is the recommended way to install DBeaver on Windows and MacOS X. It contains all required dependencies. Besides this, the installer automatically upgrades DBeaver to the new version, if a previous version is already installed.
To install DBeaver, run the installer executable and follow the instructions in its screens.

NOTE:

* The installer does not change any system settings or the Java installation. 
* The included JDK will be accessible only for DBeaver.  

### ZIP Archive
When installing DBeaver manually, without using an installer:

1. Extract the contents of the archive.  
NOTE: Do not unzip the archive over a previous DBeaver version. 
If you already have any version of DBeaver extracted in the same location - remove it before unzipping the new version.  
NOTE: All configurations, scripts and other necessary data are stored in a separate location (usually in the user`s home directory) so the program deinstallation does not affect them.

2. Run the **dbeaver** executable.

### Debian Package
To install DBeaver using a Debian package:

1. Run `sudo dpkg -i dbeaver-<version>.deb`.  
2. Execute `dbeaver &`.  

### RPM Package
To install DBeaver using RPM package:

1. Run `sudo rpm -ivh dbeaver-<version>.rpm`.  
2. Execute `dbeaver &`.  

NOTE: To upgrade DBeaver to the next version, use `sudo rpm -Uvh dbeaver-<version>.rpm` parameter.
