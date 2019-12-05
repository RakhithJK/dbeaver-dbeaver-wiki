You can perform data export/import or migration for database table(s).
We'll describe most typical use cases.

## Exporting table data to CSV format

1. Select a table(s) you want to export. In the context menu choose "Export Data".  
(Note: you also can export data from custom SQL queries results. For that in results context menu choose "Export results").
<img src="images/dt/dt-export_menu.png" width="450"/>

2. Choose export format. DBeaver support many different output formats including CSV, HTML, XLSX, etc:
<img src="images/dt/dt-export-format.png" width="450"/>

3. Set data extraction options (how data will be read from tables). This may affect extraction performance:
<img src="images/dt/dt-options-extract.png" width="450"/>

4. Set export format option. They are specific to the data format you chose on step 2:
<img src="images/dt/dt-options-format.png" width="450"/>

5. Set options for output files or clipboard:
<img src="images/dt/dt-options-output.png" width="450"/>

6. Review what and to what format you will export:
<img src="images/dt/dt-export-final.png" width="450"/>

7. Press finish. See extraction progress. Actual data extraction will be performed in background, you can keep working with your database during export process.
Note: avoid changing data in tables you selected for export while export is running.
In the end you will see status message:
<img src="images/dt/dt_message-success.png" width="200"/>

## Importing data from CSV format
You can import data from CSV file(s) directly into your database table(s).

1. Select a table(s) to which you want to import data. In the context menu choose "Import Data":
<img src="images/dt/dt-import-menu.png" width="450"/>

2. Choose import format (CSV):
<img src="images/dt/dt-import-format.png" width="450"/>

3. Select input CSV file for each table you want to import:
<img src="images/dt/dt-import-files.png" width="450"/>

4. Set CSV-to-table mappings. 
You need to set some column in CSV file for each database table column.
You can skip some column at all (in target table column value will be set to NULL).
You can set some constant value for table column if there is no source column for it in CSV.
<img src="images/dt/dt-import-mappings.png" width="450"/>

5. Set options for loading data in database. These options may affect performance:
<img src="images/dt/dt-options-load.png" width="450"/>

6. Review what file(s) and to what table(s) you will import:
<img src="images/dt/dt-import-final.png" width="450"/>

7. Press finish. See extraction progress. Actual data loading will be performed in background, you can keep working with your database during export process.
Note: avoid changing data in tables you selected for import while import is running.
In the end you will see status message:
<img src="images/dt/dt_message-success.png"/>

## Migrating table(s) data to another database table(s)

