## Schema compare/migration

You can compare two schemas/databases structure and generate report as:
- DDL script (series of create/alter/drop statements)
- Diff diagram (sort of ER diagram)
- Liquibase change log
- Liquibase change report (json or plaintext)

### Selecting objects to compare

- Select two objects (schemas, databases or tables) you want to compare
- Open context menu
- Open sub-menu `Compare/Migrate`
- Click on `Compare/Update structure` element

![](images/ug/tools/schema_compare_navigator.png)

### Compare settings

Re-validate that you chosen right objects to compare.
You can also specify which changes to process: creates, drops, alters. By default all change types are enabled.

![](images/ug/tools/schema_compare_settings.png)
