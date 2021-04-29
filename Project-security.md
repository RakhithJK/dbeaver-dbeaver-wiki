**Note: This functionality is available only in [Enterprise-Edition](Enterprise-Edition).**

DBeaver supports local storage for connection secure data. It includes:
- Database server user credentials
- SSH tunnel user credentials
- Proxy user credentials

By default, user names and passwords are stored in file `credentials-config.json`. 
This file is encrypted using the AES key. However it is really secure as this key is not secure (can be found in DBeaver sources) and thus this file can be un-encrypted by 3rd party people using some 3rd party software.

In the DBeaver Enterprise, the security support is much safer because of its strong encryption.

## Master password for local configuration

It is possible to set a master password for all projects in a local workspace.
Go to Preferences->Database->Security and enable the option `Use secure passwords storage`.
There are several password storage providers (you can see them on page General->Security->Secure Storage), `DBeaver Enterprise Password Provider` is the default one (in standalone DBeaver). It will ask you to specify master password.
DBeaver doesn't store this password anywhere, it only encrypts user credentials in a special local storage. It is not possible to decrypt this password without a password (at least easily).

The side effect of this configuration is that you cannot share your connections (with password) between different users because user credentials are stored in a completely separate location and they are protected by a local user password.

![](images/ug/workspace-security-preferences.png)

#### Use Windows Integration password provider

You can disable the default password provider and enable a "Windows Integration" provider. This provider does not need a master password but it uses a randomly generated password stored in a local user secure storage (in Windows).
This is easier (as you don't need to remember the master password) but less secure (anybody who has access to your Windows user account will have access to DBeaver's stored credentials).

## Project password

You may specify a password for a project. It will encrypt all the project's configurations with this password. Also, you will be able to share your project settings with other users (you will need to pass the project password as well).

In order to enable a project password open the project properties. You can do this by:
- Clicking on main menu File->Project security
- Clicking on "Configure" icon in the project explorer view toolbar and switching to the Project Security tab
- Pressing <kbd>ALT+Enter</kbd> on a project element in `Projects` view and switch to Project Security tab

![](images/ug/project-security-preferences.png)

On the project security page click on the "Set Password" button to enable the project password. Click on Clear to disable it (you will need to enter a current project password to clear it).

#### "Encrypt configuration" option
