Brief list of most important DBeaver shortcuts.
Of course you can redefine any (or almost any) of these shortcuts, here is the list of default values.

### SQL Editor

Shortcut|Action
--------|-----
<kbd>CTRL+Enter</kbd>|Execute current query ([*](#cur_query))
<kbd>CTRL+\\</kbd>|Execute current query in a new tab
<kbd>ALT+X</kbd>|Execute current script ([**](#cur_script))
<kbd>CTRL+ALT+SHIFT+X</kbd>|Execute queries of current script simultaneously, showing results in separate tabs
<kbd>CTRL+9</kbd>|Switch active connection (for SQL script)
<kbd>CTRL+Space</kbd> <kbd>Option+Space</kbd>|SQL completion proposals popup
<kbd>CTRL+Alt+Space</kbd>|SQL templates proposals popup
<kbd>CTRL+SHIFT+F</kbd>|Format current script ([**](#cur_script)) using current formatter
<kbd>CTRL+/</kbd> <kbd>CTRL+SHIFT+/</kbd>|Toggle single/multi line comment
<kbd>CTRL+SHIFT+X</kbd> <kbd>CTRL+SHIFT+Y</kbd>|Convert selected text into upper/lower case

### Data viewer
Shortcut|Action
--------|-----
<kbd>TAB</kbd>|Switch to record/grid mode
<kbd>CTRL+~</kbd>|Switch presentation (grid, plain text, json ,etc)
<kbd>CTRL+1</kbd>|Foreign keys navigation menu
<kbd>ALT+Space</kbd>|Navigate to the link in active cell
<kbd>ALT+Left</kbd>|Navigate backward in history
<kbd>ALT+Right</kbd>|Navigate forward in history
<kbd>CTRL+2</kbd>|Toggle sorting by current column
<kbd>F11</kbd>|Current column filters menu
<kbd>CTRL+F11</kbd>|Current column filter dictionary panel
<kbd>F7</kbd> <kbd>CTRL+7</kbd>|Toggle right panels on/off

### Database Navigator

Shortcut|Action
--------|-----
<kbd>F2</kbd>|Rename current element (if supported)
<kbd>F4</kbd>|Open editor of selected element(s)
<kbd>F5</kbd>|Refresh selected element(s)
<kbd>Delete</kbd>|Delete selected element(s) (if supported)
<kbd>CTRL+D</kbd>|Add bookmark on selected element
<kbd>Alt+Enter</kbd>|Show properties of selected element
<kbd>F3</kbd> <kbd>CTRL+[</kbd>|Open SQL editor for current connection ([***](#cur_connection)). Shows script selector popup.
<kbd>CTRL+F3</kbd> <kbd>CTRL+]</kbd>|Open new SQL editor for current connection ([***](#cur_connection)). Always creates new script.
<kbd>CTRL+Enter</kbd>|Open recent SQL editor for current connection ([***](#cur_connection)). Opens last modified script or creates a new script.

### Other

Shortcut|Action
--------|-----
<kbd>ALT+~</kbd>|Shows database tools context menu
<kbd>CTRL+0</kbd>|Switch active schema/catalog
<kbd>CTRL+SHIFT+C</kbd>|Advanced copy. Works in different context and performs "smart copy" operation (usually with parameters).

#### References

<a id="cur_query"></a>`*` - Current query is the query under cursor or the selected text. Query is separated from other script queries by delimiter   (; by default) or by empty lines.  
<a id="cur_script"></a>`**` - Current script is a set of all queries in the current SQL file. If there is a text selection then only queries in this selection are processed. Queries are separated from each other with a delimiter (; by default).  
<a id="cur_connection"></a>`**` - Current connection detected from active window and selection. If active (focused) window is SQL editor or database object editor then current connection is the same as in this editor. If active window is database navigator then active connection is "owner" connection of currently selected element. In other cases there is no current connection and DBeaver will ask you to choose connection implicitly.

