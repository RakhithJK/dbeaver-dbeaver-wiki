Sometimes (especially after multiple DBeaver versions upgrade) the workspace can become messy.  
Some keyboard shortcuts may stop working, toolbar layouts may be broken, etc, etc.  
To reset all UI settings (this includes menus, shortcuts, view and toolbar layouts):

1. Shutdown DBeaver
2. Go to the default workspace folder `.metadata\.plugins\org.eclipse.e4.workbench\`
  - Windows: <kbd>Win+R</kbd>, enter `%APPDATA%\DBeaverData\workspace6\.metadata\.plugins\org.eclipse.e4.workbench\`
  - MacOS: `open ~/Library/DBeaverData/workspace6/.metadata/.plugins/org.eclipse.e4.workbench/`
  - Linux: `cd $XDG_DATA_HOME/DBeaverData/workspace6/.metadata/.plugins/org.eclipse.e4.workbench/`
3. Delete file `workbench.xmi`
4. Start DBeaver


If that does not help then you can try to remove the `.metadata/.plugins/org.eclipse.core.resources` folder.

If that does not help then remove the `.metadata` folder. It will erase all your UI settings (but all connections, settings and scripts will remain as is). 

That is it.