Here is a shortlist of the most useful hotkeys in DBeaver UI for Windows and Linux users. It will help you work faster and more efficiently in DBeaver. 


### Connection
|Shortcut for Windows&Linux|Shortcut for macOS|Action|
|-------|-------|-------|
|F4|F4|Open object editor|
|Ctrl+Shift+D|⌃⇧D|Open database meta-object|
|Ctrl+Alt+Enter|⌃⌥↩|Open a new SQL console. No script file will be created.|
|Ctrl+]|⌃]|Create a new SQL script([***](#cur_connection))|
|F3|F3|Open existing SQL script ([***](#cur_connection))|
|Ctrl+Enter|⌃↩|Open most recent SQL script([***](#cur_connection)) for an active connection|


### Data Editor
|Shortcut for Windows&Linux|Shortcut for macOS|Action|
|-------|-------|-------|
|Alt+Insert|⌥Insert|Add new row|
|Ctrl+D|⌃D|Copy values from the row above to the current row|
|Ctrl+Alt+D|⌃⌥D|Copy values from the row below to the current row|
|Alt+Delete|⌥⌦|Delete current row|
|Ctrl+Alt+Insert|⌃⌥Insert|Duplicate current row|
|Ctrl+S|⌃S|Apply data changes|
|Ctrl+F|⌘F|Find and replace text|
|Enter|↩|Edit cell value with inline editor|
|Esc|Esc|Reset cell to the original value|
|Ctrl+Shift+Y|⇧⌘Y|Changes the selection to lowercase|
|Ctrl+Shift+X|⇧⌘X|Changes the selection to uppercase|

### SQL Editor
|Shortcut for Windows&Linux|Shortcut for macOS|Action|
|-------|-------|-------|
|Alt+X|⌥X|Execute script([**](#cur_script))|
|Ctrl+Enter|⌃↩|Execute SQL statement([*](#cur_query))|
|Ctrl+|⌃|Execute SQL statement in a new tab|
|Ctrl+Alt+Shift+X|⌃⌥⇧X|Execute script's statements in separate results tabs|
|Ctrl+/|⌃/|Add or remove the single-line comment|
|Ctrl+Shift+/|⌃⇧/|Add or remove the multi-line comment|
|Ctrl+Space|⌃Space|Enable autocomplete|

### Search
|Shortcut for Windows&Linux|Shortcut for macOS|Action|
|-------|-------|-------|
|Ctrl+H|⌃H|Open the Search dialog|
|Ctrl+Alt+Shift+F|⌥⇧⌘L|Quick search in Windows|

### Database Navigator
|Shortcut for Windows&Linux|Shortcut for macOS|Action|
|-------|-------|-------|
|Ctrl+Shift+,|⌃⇧,|Link with editor|
|F5|F5|Refresh the selected items|
|F2|F2|Rename the selected item|
|Ctrl+S|⌘S|Save changes to the current file|
|Ctrl+Shift+S|⇧⌘S|Save changes to all open files|

### Utility
|Shortcut for Windows&Linux|Shortcut for macOS|Action|
|-------|-------|-------|
|Ctrl+Shift+C|⌃⇧C|Advanced Copy|
|Ctrl+Shift+V|⌃⇧V|Paste with extra settings|

### Help
|Shortcut for Windows&Linux|Shortcut for macOS|Action|
|-------|-------|-------|
|F1|F1|Open the documentation|

Remember that you can always change the keyboard shortcut in the DBeaver settings: _Window - Preferences - User Interface - Keys._ Select command and add a keyboard shortcut to the _Binding row._


#### References

<a id="cur_query"></a>`*` - Current query is the query under cursor or the selected text. Query is separated from other script queries by delimiter   (; by default) or by empty lines.  
<a id="cur_script"></a>`**` - Current script is a set of all queries in the current SQL file. If there is a text selection then only queries in this selection are processed. Queries are separated from each other with a delimiter (; by default).  
<a id="cur_connection"></a>`**` - Current connection detected from active window and selection. If active (focused) window is SQL editor or database object editor then the current connection is the same as in this editor. If the active window is the database navigator then the active connection is the "owner" connection of the currently selected element. In other cases there is no current connection and DBeaver will ask you to choose the connection explicitly.