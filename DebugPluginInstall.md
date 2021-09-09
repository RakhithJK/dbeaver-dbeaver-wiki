## !!! This is an outdated article. Debug plugin has been included in the DBeaver CE distribution since version 5.1 !!!


# Installing Debug plugin in DBeaver CE

In order to use interactive debugging of PL/SQL procedures in DBeaver you have to install debugger plugin. Here is step-by-setp guide for install plugin from P2 repository.

**Step 0.** Run DBeaver CE 5.0.2 or higher (Debugger plugin already included in EE version you not need to install it)

**Step 1.**  Select submenu "Install new Software" from "Help" menu : 

[[/images/install_debug/Install_ext.png|]]

**Step 2.** You can see "Install new software" dialog :
[[/images/install_debug/Install_dialog.png|]]

**Step 3.** Now press add button in "Install new software" dialog and add name (for example "Dbeaver Debug") and P2 URL from Jkiss.org (https://dbeaver.io/update/debug/latest/), press "OK" button when finished:
[[/images/install_debug/Install_dialog_add.png|]]

**Step 4.** After platform finished downloading package from JKiss.org "Install" window will appear, click Next:
[[/images/install_debug/Install_debug_finished.png|]]

**Step 5.** Carefully and completely read the license agreement, select the option "I accept the terms of license agreement" if you agree with it and click Finish:

[[/images/install_debug/Install_debug_license.png|]]

**Step 6.** Now you need to accept installation by pressing "Install anyway" button :
[[/images/install_debug/Install_debug_security.png|]]

**Step 7.** Now you need accept restarting DBeaver by pressing "Restart now" button :
[[/images/install_debug/Install_debug_restart.png|]]

**Step 8.** And one more time pressing "OK" :

[[/images/install_debug/Install_debug_restart_sure.png|]]

_(Optional)_ After DBeaver restarted you can check installation of Debug plugin - select submenu "Installation details" from "Help" menu

[[/images/install_debug/Installation_details.png|Check install]]

If you can see "Dbeaver Debug" in "Installed software tab" - debug plugin installed successfuly !

[[/images/install_debug/Installation_details_check.png|Check install]]
