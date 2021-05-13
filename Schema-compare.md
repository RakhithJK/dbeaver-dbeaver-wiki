## Schema compare/migration

You can compare two schema/database structures and generate a report in the following formats:
- DDL script (series of create/alter/drop statements)
- Diff diagram (sort of ER diagram)
- Liquibase change log
- Liquibase change report (json, yaml or plaintext)

### Selecting objects to compare

- Select two objects (schemas, databases or tables) you want to compare
- Open context menu
- Open sub-menu `Compare/Migrate`
- Click on `Compare/Migrate Schema` element

![](images/ug/tools/schema_compare_navigator.png)

### Compare settings

Re-validate that you have chosen the correct objects to compare.
You can also specify the types of changes to be processed: creates, drops or alters. By default all types of changes are enabled.

![](images/ug/tools/schema_compare_settings.png)

For comparison, table containers should be used. 
Schemes - if the database supports the schemas. 
Databases if the database supports catalogs and does not support the schemes. 
Or datasourses, if there is no support schemas, nor catalog support (example is below in "Compare schemaless bases").

![](images/ug/tools/schema_compare_container_error.png)

You can exclude the specific compared types of objects.  
For example, you can do this if you do not want to see the sequences, views or external keys in the final comparison result.

![](images/ug/tools/schema_compare_settings_types.png)

### Compare results

Click on `Compare Schemas` to generate diff report.  

By default DDL diff is generated. It contains a series of create, alter and/or drop statements which will modify the schema on the right side. Thus it will make it identical to the schema on the left side.  

You can enable/disable particular changes in the tree on the left side of the diff page:

![](images/ug/tools/schema_compare_result_ddl.png)

You can also switch to another diff report representation (diagram, json, yaml, plaintext).

![](images/ug/tools/schema_compare_report_type.png)

### Compare schemaless bases

Some bases (like SQLite and Firebird) do not have catalogs and schemes that could be selected for comparison. In this case (and only for these databases), it is possible to compare the entire datasource entirely.

![](images/ug/tools/schema_compare_schemaless.png)

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
