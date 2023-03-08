**NB: This feature is available in [Enterprise](Enterprise-Edition) and [Ultimate](Ultimate-Edition) editions only.**

### Databases supporting schema comparison
* MySQL/MariaDB
* Oracle
* PostgreSQL
* SQLServer
* Snowflake
* SQLite
* Firebird
* Redshift
* DB2
* Informix
* Derby
* Greenplum
* Netezza
* Cockroach
* Vertica
* SAP HANA
* Databricks
* Teradata
* YugabyteDB
* EnterpriseDB

You can compare two schema/database structures and generate a report in the following formats:
- DDL script (series of create/alter/drop statements)
- Diff diagram (sort of ER diagram)
- Liquibase changelog
- Liquibase change report (JSON, YAML, or plaintext)

### Selecting objects to compare

- Select the two objects (schemas, databases, or tables) you want to compare
- Open the context menu
- Open the sub-menu `Compare/Migrate`
- Click on the `Compare/Migrate Schema` element

![](images/ug/tools/schema_compare_navigator.png)

### Compare settings

Re-validate that you have chosen the correct objects to compare.
You can click the `Settings` button to access the global preferences window.
Or click the `Swap sources` button to change places of target and source containers in the view.

![](images/ug/tools/schema_compare_settings.png)

For comparisons, table containers should be used.
 
Schemes - if the database supports the schemas. 
Databases - if the database supports catalogs and does not support the schemes. 
Datasources - if there is no support schemas or catalog support (you can find an example below in "Compare schemaless databases").

![](images/ug/tools/schema_compare_container_error.png)

On the next page (after clicking on the `Next` button), you can see compare process settings.
Enabling the `Export result to the file` checkbox will lead to the fact that the comparison/changelog results will be saved as a file.
A hint about available variables for a pattern will arise when a cursor on the entry field of the file name is entered.
Choose the report format in the `Report Engine` combo box. The changes will be immediately applied to the pattern of the file name.

![](images/ug/tools/schema_compare_change_engine.png)

You can also specify the changes to be processed: create, drop, or alter. By default, all kinds of changes are enabled. If you do not want to compare objects with equal names but in different cases (like "test" and "TesT") - you can enable the `Case insensitive compare`.
(Note: This settings section is unavailable for the generation changelog process).

Also, you can simply exclude the specific compared types of objects.  
For example, you can do this without seeing the sequences, views, or external keys in the final comparison result.

![](images/ug/tools/schema_compare_settings_types.png)

### Compare results

Click on `Proceed` to generate a diff report.  

By default, DDL diff is generated. It contains a series of creating, altering, and/or dropping statements that will modify the schema on the right side. Thus it will make it identical to the schema on the left side.  

You can enable/disable certain changes in the tree on the left side of the diff page:

![](images/ug/tools/schema_compare_result_ddl.png)

Use the `Refresh Report` button after objects change in the left tree to refresh the report on the right side.

You can view all changes in the SQL Editor with the help of the `Open in Editor` button.

If you definitely shore that compared changes should be applied to a target container, click on the `Migrate` button. And all generated SQL statements will be executed in a target container.

Click on the `Report type` combo box if you can switch to another diff report representation (diagram, JSON, YAML, plaintext).

![](images/ug/tools/schema_compare_report_type.png)

The `Save` button allows you to save the report as a file of the format chosen step earlier.

### Compare logs

To get acquainted with the comparison logs, you first specify the logging level on the Preferences-> Editors-> Schema Compare preference page. Specify one of the logging levels and click on `Apply`. By default, the logging level is the OFF level. To get complete information, you can choose the DEBUG level.

![](images/ug/tools/schema_compare_log_levels.png)

After comparing operations, click the `Show log` button. A log will be open in the Editor, and the content of this log will depend on the logging level you choose in the settings. Log level сhanges from preferences will not be applied to the comparison wizard if it is already open in another window. Close and open the schema compare wizard in this case.

![](images/ug/tools/schema_compare_show_logs.png)

### Compare schemaless bases

Some bases (like SQLite and Firebird) do not have catalogs and schemes that can be selected for comparison. In this case (and only for these databases), it is possible to compare the entire datasource.

![](images/ug/tools/schema_compare_schemaless.png)

### Extra preferences

For the objects in the report to be dressed in quotation marks, you can choose the `Quote all objects names` in the settings.

![](images/ug/tools/schema_compare_preferences.png)

### Liquibase Changelog generation

Suppose you want to create a report about your table container objects (similar to the metadata dump operation). In that case, you can choose in the navigator tree on your container - `Compare/Migrate` -> `Liquibase changelog` command. 

![](images/ug/tools/schema_changelog_input.png)

One or several table containers can be chosen. The report will contain creation statements of tables/views/keys/sequences - metadata from the table containers. But without data from tables/views. You can use this report in the future to restore the structure of your database.

![](images/ug/tools/schema_changelog_result.png)

### Using schema compare with Liquibase PRO key.

If you have a Liquibase PRO key, then you can use it with DBeaver.
Steps you need:
- Find and open your dbeaver.ini file. It is located in the DBeaver root directory.
- Find -vmargs command
- Add a new line after this command: -Dliquibase.license.key=yourKey (example: -Dliquibase.license.key=ABwwGgQU...)
- Open DBeaver and the "Schema compare" window. The key will be checked at this step.

You can also add the Liquibase Pro key via UI in Preferences->Editors->Schema Compare preference page.
Use the `Import Liquibase Pro Key` button to open the Import key dialog.

![](images/ug/tools/schema_compare_import_LB_key_button.png)

You can manually add your key in the Liquibase Key text field, throw the `Paste` button, or use the `Load` button to download a file.
You can check the license state with the `Check Key State` button. After pressing the button, you can see the result of the checking in the `Messages` field.

![](images/ug/tools/schema_compare_import_LB_dialog_ivalid_state.png)

![](images/ug/tools/schema_compare_import_LB_dialog_valid_state.png)

We suggest you restart the program after adding a key for the correct program work. Settings сhanges will not be applied to the comparison wizard if it is already open in another window. The key will be saved in the DBeaver settings. If you specify the key in the .ini file and install another key through the Import Key dialog, the key from the .ini file will be in priority.

If the license key is valid, the `Object types` dialog will be extended to PRO objects.
(If PRO objects didn't appear in the schema compare changelog - check your logs. Maybe the license expired, or the key is invalid)

![](images/ug/tools/schema_compare_settings_PRO_types.png)

### Object types being compared by LiquibasePRO

- Check Constraints
- Procedures
- Functions
- Triggers
- Synonyms (Oracle)
- Package with the body (Oracle)
