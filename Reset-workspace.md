Sometimes (especially after multiple DBeaver versions upgrade) workspace become messy.  
Some keyboard shortcuts may stop working, toolbars layout may be broken, etc, etc.  
To reset all UI settings (this includes menus, shortcuts, view and toolbar layouts):

1. Shutdown DBeaver
2. Go to directory to workspace folder `.metadata\.plugins\org.eclipse.e4.workbench\`
  - Windows: `Win+R`, enter `%APPDATA%\DBeaverData\workspace6\.metadata\.plugins\org.eclipse.e4.workbench\`
  - Linux: `cd $XDG_DATA_HOME/DBeaverData/workspace6/.metadata/.plugins/org.eclipse.e4.workbench/`
  - MacOS: `open ~/Library/DBeaverData/workspace6/.metadata/.plugins/org.eclipse.e4.workbench/`
3. Delete file `workbench.xmi`
4. Start DBeaver

If that doesn't help then you can try to remove `%HOMEPATH%\.dbeaver4\.metadata\` folder. 
This will erase all your UI settings and SQL scripts configurations (but all connections and scripts will remain). Do it only if nothing else helps!

That's it.