Sometimes, usually after multiple version and /or upgrades/incorrect shutdowns DBeaver UI may become corrupted.
Extra toolbar elements, missing menu items, broken keyboard shortcuts, broken localization strings and other glitches may happen.

To reset DBeaver UI just delete file file `workbench.xmi` in DBeaver workspace/.metadata.
DBeaver workspace default location is in user home subfolder `.dbeaver4`.
So default workbench.xmi file locations is:
- Windows: `%HOMEPATH%\.dbeaver4\.metadata\.plugins\org.eclipse.e4.workbench\workbench.xmi`
- MacOS and Linux: `~/.dbeaver4/.metadata/.plugins/org.eclipse.e4.workbench/workbench.xmi`

To reset settings:

1. Close DBeaver
2. Open terminal and run `del` (Windows) or `rm` (Linux/MacOS) followed by workbench.xmi path.
3. Start DBeaver
