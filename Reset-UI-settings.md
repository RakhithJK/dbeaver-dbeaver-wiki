Sometimes, usually after multiple version and /or upgrades/incorrect shutdowns DBeaver UI may become corrupted.
Extra toolbar elements, missing menu items, broken keyboard shortcuts, broken localization strings and other glitches may happen.

To reset DBeaver UI just delete file `workbench.xmi` in DBeaver workspace/.metadata.
By default workbench.xmi file locations is:

- Windows: `%APPDATA%\DBeaverData\workspace6\.metadata\.plugins\org.eclipse.e4.workbench\workbench.xmi`
- MacOS: `~/Library/DBeaverData/workspace6/.metadata/.plugins/org.eclipse.e4.workbench/workbench.xmi`
- Linux: `$XDG_DATA_HOME/DBeaverData/workspace6/.metadata/.plugins/org.eclipse.e4.workbench/workbench.xmi`

To reset settings:

1. Close DBeaver
2. Delete workbench.xmi from Explorer/Finder or open terminal and run `del` (Windows) or `rm` (Linux/MacOS) followed by workbench.xmi path.
3. Start DBeaver
