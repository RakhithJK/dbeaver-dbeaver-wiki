This guide describes how to set up application preferences through configuration files without even booting it up.

### Locating preference files

Preference files have the extension `.prefs` and can be found in the [workspace](Workspace-Location) directory under the
following path:
`.metadata/.plugins/org.eclipse.core.runtime/.settings`

You might not find a preference file you're interested in if it hasn't been created yet. In that case, you will need to
create one yourself. See the examples below to figure out which preference file you need.

### Reading and modifying preference files

Preference files consist of key-value pairs glued together with `=` and separated with a line break:

```properties
# file org.jkiss.dbeaver.test.prefs
some.key=value1
some.other.key=value2
```  

You can place the following preferences in the `org.jkiss.dbeaver.core.prefs` file:  

### Default navigator view for new connections


Name|Type|Default Value|Allowed Values|Description
----|----|-------------|--------------|-----------
navigator.settings.default.preset|string|`simple`|`simple`, `advanced`|Sets the default view mode for new connections<br>Don't specify this preference if you want to configure a custom preset.
navigator.settings.default.showSystemObjects|boolean|`false`|`true`, `false`|Controls whether system objects must be shown.<br>Used if preset is not specified.
navigator.settings.default.showUtilityObjects|boolean|`false`|`true`, `false`|Controls whether utility objects must be shown.<br>Used if preset is not specified.
navigator.settings.default.showOnlyEntities|boolean|`false`|`true`, `false`|Controls whether only schemas and tables must be shown.<br>Used if preset is not specified.
navigator.settings.default.mergeEntities|boolean|`false`|`true`, `false`|Controls whether all tables must be shown in a single list.<br>Used if preset is not specified.

For more information, please see [Simple and Advanced View](Simple-and-Advanced-View).

### Miscellaneous [[navigator settings|Database-Navigator]]

Name|Type|Default Value|Allowed Values|Description
----|----|-------------|--------------|-----------
navigator.settings.default.connectionPattern | string | `host_or_database` | expression with variables | Pattern for new connections title
navigator.show.folder.placeholders | boolean | `true` | `true`, `false` | Show placeholders for special folders (e.g. Scripts)
navigator.sort.case.insensitive | boolean | `true` | `true`, `false` | Sort items in case-insensitive mode
navigator.sort.forlers.first | boolean | `true` | `true`, `false` | Show folders first

### Default [[transaction settings|Auto-and-Manual-Commit-Modes]]

Name|Type|Default Value|Allowed Values|Description
----|----|-------------|--------------|-----------
transaction.smart.commit | boolean | `false` | `true`, `false` | Enable smart commit mode
transaction.smart.commit.recover | boolean | `true` | `true`, `false` | Return to auto-commit mode after transaction end
transaction.auto.close.enabled | boolean | `false` | `true`, `false` | Automatically end (rollback) transaction after idle period
transaction.auto.close.ttl | integer | `900` | integer value | Timeout before transaction close
transaction.show.notifications | boolean | `true` | `true`, `false` | Show folders first

### Metadata settings

 Name                              | Type    | Default Value | Allowed Values    | Description                                                                                                                               
-----------------------------------|---------|---------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------
 database.meta.separate.connection | string  | `DEFAULT`           | `ALWAYS`, `NEVER` | Controls whether to open a separate connection for metadata read. <br> Don't specify this preference if you want to use default settings. 
 database.meta.casesensitive       | boolean | `false`          | `true`, `false`   | Specifies the usage of case-sensitive names in DDL statements.                                                                            
 database.props.expensive          | boolean | `true`          | `true`, `false`   | Enables display of row count for tables.                                                                                                  
 database.meta.server.side.filters | boolean | `true`          | `true`, `false`   | Enables display of server-side object filters.                                                                                                                                                  

### [Query manager](Query-Manager) settings

 Name            | Type    | Default Value | Allowed Values                                                     | Description                                           
-----------------|---------|---------------|--------------------------------------------------------------------|-------------------------------------------------------
 qm.queryTypes   | string  | `USER`, `USER_FILTERED`, `USER_SCRIPT`           | `USER`, `USER_FILTERED`, `USER_SCRIPT`,<br> `UTIL`, `META`, `META_DDL` | View for different query types.       
 qm.objectTypes  | string  | `session`,`txn`,`query`           | `session`,`txn`,`query`                                                  | View for different object types.      
 qm.maxEntries   | integer | `200`           | integer value                                                      | Number of entries displayed per page. 
 qm.storeLogs    | boolean | `false`         | `true`, `false`                                                      | Enables the saving of logs.                 
 qm.logDirectory | string  | [workspace directory](Workspace-Location)           | string value                                                       | Folder location for saving logs.          
 qm.historyDays  | integer | `90`           | integer value                                                      | Number of days for storing logs.          

### [Database Navigator](Database-Navigator) settings

 Name                                  | Type    | Default Value   | Allowed Values                                                                                                                       | Description                                                    
---------------------------------------|---------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------
 navigator.show.connection.host        | boolean | `true`            | `true`, `false`                                                                                                                      | Display the connection host name.                   
 navigator.show.objects.description    | boolean | `false`           | `true`, `false`                                                                                                                      | Display the objects description.                    
 navigator.show.statistics.info        | boolean | `true`            | `true`, `false`                                                                                                                      | Display the statistic info.                         
 navigator.show.node.actions           | boolean | `true`            | `true`, `false`                                                                                                                      | Display the actions icons.                          
 navigator.show.folder.placeholders    | boolean | `true`            | `true`, `false`                                                                                                                      | Display placeholders for special folders.           
 navigator.sort.forlers.first          | boolean | `true`            | `true`, `false`                                                                                                                      | Display folders first.                              
 navigator.sort.case.insensitive       | boolean | `false`           | `true`, `false`                                                                                                                      | Order elements alphabetically.                      
 navigator.color.nodes.all             | boolean | `false`           | `true`, `false`                                                                                                                      | Set connection color for all elements.              
 navigator.show.objects.tips           | boolean | `true`            | `true`, `false`                                                                                                                      | Display objects modifiers in tree.                  
 navigator.show.tooltips               | boolean | `true`            | `true`, `false`                                                                                                                      | Display tooltips.                                   
 navigator.show.tooltips.file.contents | boolean | `false`           | `true`, `false`                                                                                                                      | Display file contents in tooltips.                  
 navigator.object.doubleClick          | string  | `EDIT` | `EXPAND`                                                                                                                             | The behavior on double-clicking a node.            
 navigator.connection.doubleClick      | string  | `EXPAND`          | `EDIT`,<br> `CONNECT`,<br> `SQL_EDITOR`,<br> `SQL_EDITOR_NEW`                                                                                   | SThe behavior on double-clicking on connection.     
 navigator.object.defaultEditorPage    | string  | `""`     | <font size= “1”>`default.object.editor`,<br>`org.jkiss.dbeaver.ui.editors.data.DatabaseDataEditor`,<br>`org.jkiss.dbeaver.erd.ui.editor.ERDEditorEmbedded`</font>| The behavior of default editor page.               
 navigator.expand.on.connect           | boolean | `false`           | `true`, `false`                                                                                                                      | Expand navigator tree on connect.                 
 navigator.restore.filters             | boolean | `false`           | `true`, `false`                                                                                                                      | Database navigator filter.             
 navigator.long.list.fetch.size        | integer | `5000`            | integer values                                                                                                                       | Elements fetch size.                              
 navigator.restore.state.depth         | integer | `0`               | integer values                                                                                                                       | Restore the navigator state up to a certain depth. 

### [Error Logs](Log-files) settings

 Name                       | Type    | Default Value                              | Allowed Values  | Description                                 
----------------------------|---------|--------------------------------------------|-----------------|---------------------------------------------
 logs.debug.enabled         | boolean | `true`                                       | `true`, `false` | Enable debug logs.               
 logs.debug.location        | string  | `${workspace}/.metadata/dbeaver-debug.log` | string values   | Location of the log save file.  
 logs.files.output.maxSize  | integer | `10485760`                                   | integer values  | Maximum log file size (KB).     
 logs.files.output.maxCount | integer | `3`                                          | integer values  | Maximum backup log files count. 

### User Interface settings

 Name                     | Type    | Default Value | Allowed Values                                                                    | Description                                     
--------------------------|---------|---------------|-----------------------------------------------------------------------------------|-------------------------------------------------
 ui.auto.update.check     | boolean | `true`          | `true`, `false`                                                                   | Enable automatic updates check.      
 platform.language        | string  | `en`          | `en`,  `zh_CN`,  `ru`,  `fr`,  `de`,<br>  `it`,  `ja`,  `es`,  `pt`,  `ko`,  `zh_TW`, | Platform language setting.                      
 java.client.timezone     | string  | operating system time zone           | [time zones](JDBC-Time-Zones)                                          | Time zone setting.                              
 notifications.enabled    | boolean | `true`          | `true`, `false`                                                                   | Popup notification setting.                     
 notifications.closeDelay | integer | `3000`          | integer values                                                                    | Popup window automatic hide delay setting (ms). 

### [SQL Editor](SQL-Editor) settings

 Name                                                  | Type    | Default Value | Allowed Values                         | Description                                                                    
-------------------------------------------------------|---------|---------------|----------------------------------------|--------------------------------------------------------------------------------
 database.editor.separate.connection                   | string  | `DEFAULT`          | `ALWAYS`, `NEVER`                      | Opening a separate connection for each editor.                 
 database.editor.connect.on.activate                   | boolean | `true`          | `true`, `false`                        | Connect on editors activation.                                 
 database.editor.connect.on.execute                    | boolean | `false`         | `true`, `false`                        | Connect on query execute.                                      
 SQLEditor.autoSaveOnChange                            | boolean | `false`         | `true`, `false`                        | Auto-save after any modifications.                             
 SQLEditor.autoSaveOnClose                             | boolean | `false`         | `true`, `false`                        | Auto-save editor on close.                                     
 SQLEditor.autoSaveOnExecute                           | boolean | `false`         | `true`, `false`                        | Save editor on query execute.                                  
 SQLEditor.autoSaveActiveSchema                        | boolean | `true`          | `true`, `false`                        | Save/restore active schema.                                    
 SQLEditor.resultSet.closeOnError                      | boolean | `false`         | `true`, `false`                        | Close results tab on error.                                    
 SQLEditor.resultSet.replaceCurrentTab                 | boolean | `true`          | `true`, `false`                        | Replace active result tab on single query execution.           
 SQLEditor.resultSet.orientation                       | string  | `HORIZONTAL`    | `VERTICAL`                             | Result orientation view.                                       
 SQLEditor.outputPanel.autoShow                        | boolean | `true`          | `true`, `false`                        | Open output viewer on new messages.                            
 SQLEditor.outputPanel.autoShow                        | integer | `20`            | integer values                         | Set maximum of result tabs for single query.                   
 SQLEditor.ContentAssistant.auto.activation.enable     | boolean | `true`          | `true`, `false`                        | Enable auto activation in SQL assistant.                       
 SQLEditor.ContentAssistant.activate.hippie            | boolean | `false`         | `true`, `false`                        | Activate Hippie Engine for autocompletition in SQL assistant.  
 SQLEditor.ContentAssistant.auto.activation.delay      | integer | `0`             | integer values                         | Auto activate delay (ms).                                      
 SQLEditor.ContentAssistant.auto.keystrokes.activation | boolean | `true`          | `true`, `false`                        | Activate SQL assistant on typing.                              
 SQLEditor.ContentAssistant.insert.single.proposal     | boolean | `true`          | `true`, `false`                        | Auto insert proposal in SQL assistant.                         
 SQLEditor.ContentAssistant.autocompletion.tab         | boolean | `true`          | `true`, `false`                        | Use Tab for autocompletition in SQL assistant.                 
 SQLEditor.ContentAssistant.insert.case                | integer | `0`           | `1`, `2`                                   | Insert case in SQL assistant (1- Upper case, 2 - Lower case).  
 SQLEditor.ContentAssistant.replace.word               | boolean | `false`         | `true`, `false`                        | Replace current word in SQL assistant.                         
 SQLEditor.ContentAssistant.hide.duplicates            | boolean | `false`         | `true`, `false`                        | Hide duplicate names from non-active schemas in SQL assistant. 
 SQLEditor.ContentAssistant.proposals.short.name       | boolean | `false`         | `true`, `false`                        | Use short object names in SQL assistant.                       
 SQLEditor.ContentAssistant.show.helpTopics            | boolean | `false`         | `true`, `false`                        | Show server help topics in SQL assistant.                      
 SQLEditor.ContentAssistant.show.values                | boolean | `true`          | `true`, `false`                        | Show values in SQL assistant.                                  
 sql.proposals.insert.table.alias                      | string  | `PLAIN`           | `NONE`, `EXTENDED`                     | Insert table aliases (in FROM clauses).                        
 SQLEditor.format.activeQuery                          | boolean | `true`          | `true`, `false`                        | Enable format active query only.                                                                                    
 script.auto.folders                                   | boolean | `false`         | `true`, `false`                        | Create script folder for each connection.                      