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
navigator.settings.default.preset|string|N/A or `simple` (Lite Edition)|`simple`, `advanced`|Sets the default view mode for new connections<br>Don't specify this preference if you want to configure a custom preset.
navigator.settings.default.showSystemObjects|boolean|N/A|`true`, `false`|Controls whether system objects must be shown.<br>Used if preset is not specified.
navigator.settings.default.showUtilityObjects|boolean|N/A|`true`, `false`|Controls whether utility objects must be shown.<br>Used if preset is not specified.
navigator.settings.default.showOnlyEntities|boolean|N/A|`true`, `false`|Controls whether only schemas and tables must be shown.<br>Used if preset is not specified.
navigator.settings.default.mergeEntities|boolean|N/A|`true`, `false`|Controls whether all tables must be shown in a single list.<br>Used if preset is not specified.

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
 database.meta.separate.connection | string  | N/A           | `ALWAYS`, `NEVER` | Controls whether to open a separate connection for metadata read. <br> Don't specify this preference if you want to use default settings. 
 database.meta.casesensitive       | boolean | `true`          | `true`, `false`   | Specifies the usage of case-sensitive names in DDL statements.                                                                            
 database.props.expensive          | boolean | `true`          | `true`, `false`   | Enables display of row count for tables.                                                                                                  
 database.meta.server.side.filters | boolean | `true`          | `true`, `false`   | Enables display of server-side object filters.                                                                                                                                                  

### [Query manager](Query-Manager) settings

 Name            | Type    | Default Value | Allowed Values                                                     | Description                                           
-----------------|---------|---------------|--------------------------------------------------------------------|-------------------------------------------------------
 qm.queryTypes   | string  | N/A           | `USER`, `USER_FILTERED`, `USER_SCRIPT`,<br> `UTIL`, `META`, `META_DDL` | Settings of the view for different query types.       
 qm.objectTypes  | string  | N/A           | `session`,`txn`,`query`                                                  | Settings of the view for different object types.      
 qm.maxEntries   | integer | `200`           | integer value                                                      | Settings of the number of entries displayed per page. 
 qm.storeLogs    | boolean | `false`         | `true`, `false`                                                      | Setting that allows you to save logs.                 
 qm.logDirectory | string  | N/A           | string value                                                       | Setting the folder location for saving logs.          
 qm.historyDays  | integer | N/A           | integer value                                                      | Setting the number of days for storing logs.          

### [Database Navigator](Database-Navigator) settings

 Name                                  | Type    | Default Value   | Allowed Values                                                                                                                       | Description                                                    
---------------------------------------|---------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------
 navigator.show.connection.host        | boolean | `true`            | `true`, `false`                                                                                                                      | Setting to display the connection host name.                   
 navigator.show.objects.description    | boolean | `false`           | `true`, `false`                                                                                                                      | Setting to display the objects description.                    
 navigator.show.statistics.info        | boolean | `true`            | `true`, `false`                                                                                                                      | Setting to display the statistic info.                         
 navigator.show.node.actions           | boolean | `true`            | `true`, `false`                                                                                                                      | Setting to display the actions icons.                          
 navigator.show.folder.placeholders    | boolean | `true`            | `true`, `false`                                                                                                                      | Setting to display placeholders for special folders.           
 navigator.sort.forlers.first          | boolean | `true`            | `true`, `false`                                                                                                                      | Setting to display folders first.                              
 navigator.sort.case.insensitive       | boolean | `false`           | `true`, `false`                                                                                                                      | Setting to order elements alphabetically.                      
 navigator.color.nodes.all             | boolean | `false`           | `true`, `false`                                                                                                                      | Setting to set connection color for all elements.              
 navigator.show.objects.tips           | boolean | `true`            | `true`, `false`                                                                                                                      | Setting to display objects modifiers in tree.                  
 navigator.show.tooltips               | boolean | `true`            | `true`, `false`                                                                                                                      | Setting to display tooltips.                                   
 navigator.show.tooltips.file.contents | boolean | `false`           | `true`, `false`                                                                                                                      | Setting to display file contents in tooltips.                  
 navigator.object.doubleClick          | string  | `Open properties` | `EXPAND`                                                                                                                             | Setting for the behavior on double-clicking a node.            
 navigator.connection.doubleClick      | string  | `Expand`          | `EDIT`,<br> `CONNECT`,<br> `SQL_EDITOR`,<br> `SQL_EDITOR_NEW`                                                                                   | Setting for the behavior on double-clicking on connection.     
 navigator.object.defaultEditorPage    | string  | `Last opened`     | <font size= “1”>`default.object.editor`,<br>`org.jkiss.dbeaver.ui.editors.data.DatabaseDataEditor`,<br>`org.jkiss.dbeaver.erd.ui.editor.ERDEditorEmbedded`</font>| Setting for the behavior of default editor page.               
 navigator.expand.on.connect           | boolean | `false`           | `true`, `false`                                                                                                                      | Settings for expand navigator tree on connect.                 
 navigator.restore.filters             | boolean | `false`           | `true`, `false`                                                                                                                      | Settings for saving the database navigator filter.             
 navigator.long.list.fetch.size        | integer | `5000`            | integer values                                                                                                                       | Settings for elements fetch size.                              
 navigator.restore.state.depth         | integer | `0`               | integer values                                                                                                                       | Settings to restore the navigator state up to a certain depth. 

### [Error Logs](Log-files) settings

 Name                       | Type    | Default Value                              | Allowed Values  | Description                                 
----------------------------|---------|--------------------------------------------|-----------------|---------------------------------------------
 logs.debug.enabled         | boolean | `true`                                       | `true`, `false` | Setting to enable debug logs.               
 logs.debug.location        | string  | `${workspace}/.metadata/dbeaver-debug.log` | string values   | Setting the location of the log save file.  
 logs.files.output.maxSize  | integer | `10485760`                                   | integer values  | Setting the maximum log file size (KB).     
 logs.files.output.maxCount | integer | `3`                                          | integer values  | Setting the maximum backup log files count. 

### User Interface settings

 Name                     | Type    | Default Value | Allowed Values                                                                    | Description                                     
--------------------------|---------|---------------|-----------------------------------------------------------------------------------|-------------------------------------------------
 ui.auto.update.check     | boolean | `true`          | `true`, `false`                                                                   | Setting to enable automatic updates check.      
 platform.language        | string  | `en`          | `en`,  `zh_CN`,  `ru`,  `fr`,  `de`,<br>  `it`,  `ja`,  `es`,  `pt`,  `ko`,  `zh_TW`, | Platform language setting.                      
 java.client.timezone     | string  | N/A           | values from `java.util.TimeZone` package                                          | Time zone setting.                              
 notifications.enabled    | boolean | `true`          | `true`, `false`                                                                   | Popup notification setting.                     
 notifications.closeDelay | integer | `3000`          | integer values                                                                    | Popup window automatic hide delay setting (ms). 

### [SQL Editor](SQL-Editor) settings

 Name                                                  | Type    | Default Value | Allowed Values                         | Description                                                                    
-------------------------------------------------------|---------|---------------|----------------------------------------|--------------------------------------------------------------------------------
 database.editor.separate.connection                   | string  | N/A           | `ALWAYS`, `NEVER`                      | The setting for opening a separate connection for each editor.                 
 database.editor.connect.on.activate                   | boolean | `true`          | `true`, `false`                        | The setting for connect on editors activation.                                 
 database.editor.connect.on.execute                    | boolean | `false`         | `true`, `false`                        | The setting for connect on query execute.                                      
 SQLEditor.autoSaveOnChange                            | boolean | `false`         | `true`, `false`                        | The setting for auto-save after any modifications.                             
 SQLEditor.autoSaveOnClose                             | boolean | `false`         | `true`, `false`                        | The setting for auto-save editor on close.                                     
 SQLEditor.autoSaveOnExecute                           | boolean | `false`         | `true`, `false`                        | The setting for save editor on query execute.                                  
 SQLEditor.autoSaveActiveSchema                        | boolean | `true`          | `true`, `false`                        | The setting for save/restore active schema.                                    
 SQLEditor.resultSet.closeOnError                      | boolean | `false`         | `true`, `false`                        | The setting for close results tab on error.                                    
 SQLEditor.resultSet.replaceCurrentTab                 | boolean | `true`          | `true`, `false`                        | The setting for replace active result tab on single query execution.           
 SQLEditor.resultSet.orientation                       | string  | `Horizontal`    | `VERTICAL`                             | The setting for result orientation view.                                       
 SQLEditor.outputPanel.autoShow                        | boolean | `true`          | `true`, `false`                        | The setting for open output viewer on new messages.                            
 SQLEditor.outputPanel.autoShow                        | integer | `20`            | integer values                         | The setting for set maximum of result tabs for single query.                   
 SQLEditor.ContentAssistant.auto.activation.enable     | boolean | `true`          | `true`, `false`                        | The setting for enable auto activation in SQL assistant.                       
 SQLEditor.ContentAssistant.activate.hippie            | boolean | `false`         | `true`, `false`                        | The setting for activate Hippie Engine for autocompletition in SQL assistant.  
 SQLEditor.ContentAssistant.auto.activation.delay      | integer | `0`             | integer values                         | The setting for auto activate delay (ms).                                      
 SQLEditor.ContentAssistant.auto.keystrokes.activation | boolean | `true`          | `true`, `false`                        | The setting for activate SQL assistant on typing.                              
 SQLEditor.ContentAssistant.insert.single.proposal     | boolean | `true`          | `true`, `false`                        | The setting for auto insert proposal in SQL assistant.                         
 SQLEditor.ContentAssistant.autocompletion.tab         | boolean | `true`          | `true`, `false`                        | The setting for use Tab for autocompletition in SQL assistant.                 
 SQLEditor.ContentAssistant.insert.case                | integer | N/A           | `1`, `2`                                   | The setting for insert case in SQL assistant (1- Upper case, 2 - Lower case).  
 SQLEditor.ContentAssistant.replace.word               | boolean | `false`         | `true`, `false`                        | The setting for replace current word in SQL assistant.                         
 SQLEditor.ContentAssistant.hide.duplicates            | boolean | `false`         | `true`, `false`                        | The setting for hide duplicate names from non-active schemas in SQL assistant. 
 SQLEditor.ContentAssistant.proposals.short.name       | boolean | `false`         | `true`, `false`                        | The setting for use short object names in SQL assistant.                       
 SQLEditor.ContentAssistant.show.helpTopics            | boolean | `false`         | `true`, `false`                        | The setting for show server help topics in SQL assistant.                      
 SQLEditor.ContentAssistant.show.values                | boolean | `true`          | `true`, `false`                        | The setting for show values in SQL assistant.                                  
 sql.proposals.insert.table.alias                      | string  | N/A           | `NONE`, `EXTENDED`                     | The setting for insert table aliases (in FROM clauses).                        
 SQLEditor.format.activeQuery                          | boolean | `true`          | `true`, `false`                        | Setting to enable format active query only.                                    
 sql.format.formatter                                  | string  | N/A           | `COMPACT`,<br>`EXTERNAL`,<br>`SQLWORKBENCHJ` | Formatter display setting.                                                     
 script.auto.folders                                   | boolean | `false`         | `true`, `false`                        | The setting for create script folder for each connection.                      