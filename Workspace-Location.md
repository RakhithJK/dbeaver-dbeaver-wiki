### Default location of DBeaver workspace 
By default DBeaver stores all its files (configurations, scripts, diagrams, etc) in the following folder:

OS | Location
---|---
Windows | `%APPDATA%\DBeaverData\`
MacOS | `~/Library/DBeaverData/`
Linux | `$XDG_DATA_HOME/DBeaverData/` ($XDG_DATA_HOME=`~/.local/share` if not set)

#### Folders

Folder | Location
---|---
`workspace6` | Workspace files for DBeaver 6.1+
`drivers` | Auto downloaded database drivers

### Custom location

You can specify a custom workspace location by passing parameter `-data <path>` in the command line. `<path>` can be an absolute or relative directory path.

### Old (before DBeaver 6.1.3) default workspace location

OS | Location
---|---
Windows | `C:\Users\YourName\.dbeaver4`.
Linux | `~/.dbeaver4/`
MacOS | `~/.dbeaver4/`

### Ancient (before DBeaver 4) default workspace location

OS | Location
---|---
Windows | `C:\Users\YourName\.dbeaver`.
Linux | `~/.dbeaver/`
MacOS | `~/.dbeaver/`
