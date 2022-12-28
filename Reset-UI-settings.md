## Reset UI settings

You might want to reset UI settings in the following cases:
- Shortcuts suddenly stop working
- Theme colors are messed up
- Broken or invalid localization
- Other UI elements aren't shown anymore

This can happen due to the following reasons:
- After multiple version upgrades
- After switching between newer and older versions
- After an incorrect shutdown

You can perform a reset using the <kbd>Help</kbd> &rArr; <kbd>Reset UI Settings...</kbd> action.

> **Be careful**: this will reset **all** UI settings and other user preferences, including:
> - layout of menus, toolbars, windows, editors
> - theme, colors, and fonts
> - other settings from installed third-party plugins

After accepting the confirmation, DBeaver will restart and greet you with a fresh workspace.

### Manual reset

If you cannot launch DBeaver, you can reset the workspace manually.

** Be careful**: only delete any other files if you know what you're doing, and follow the steps below. 

To do so, do the following:
1. - On **Windows**, open Explorer and navigate to `%APPDATA%\DBeaverData\workspace6\.metadata\.plugins`
   - On **macOS**, open Finder and navigate to `~/Library/DBeaverData/workspace6/.metadata/.plugins`
   - On **Linux**, open file explorer and navigate to `$XDG_DATA_HOME/DBeaverData/workspace6/.metadata/.plugins`
1. First, you can try deleting the file `workbench.xmi` located in the `org.eclipse.e4.workbench` directory
1. If it didn't help, you could delete all files in the `.plugins` directory or that directory itself

## Clear History

You can clean up the workspace by deleting redundant files that accumulate as you use DBeaver.

You do so, use the <kbd>Help</kbd> &rArr; <kbd>Clear History...</kbd> action.

You will need to choose one or more options provided below:

|Name|Description|
|---|---|
|Task run history|Contains information about previously run tasks along with logs collected during their execution|
|Query log history <img src="images/commercial.png" vspace="4" align="top" alt="Query history is not persisted between sessions in the community edition"/>|Contains information about previously run (user and meta) SQL queries|

When you're happy with the options, click the `Apply and Restart` button to continue.