You can perform data export/import or migration for database table(s).
We will describe most typically used cases.

## Exporting table data to CSV format

1. Select a table or tables you want to export. In the context menu choose "Export Data".  
(Note: you can also export data from custom SQL queries results. To do that, choose "Export results" in the results context menu).
![](images/dt/dt-export_menu.png)

2. Choose export format. DBeaver supports many different output formats including CSV, HTML, XLSX, etc:
![](images/dt/dt-export-format.png)

3. Set data extraction options (how the data will be read from the tables). This may affect the extraction's performance.
And set export format option. They are specific to the data format you chose on step 2:
![](images/dt/dt-options-extract.png)

6. Set options for output files or clipboard. 
Note: Timestamp pattern is used here to target the file name pattern:
![](images/dt/dt-options-output.png)

7. Review what you want to format and into which format you will export it. You can also save all your settings as a task in this step or change the task variables:
![](images/dt/dt-export-final.png)

8. Press finish. See extraction progress. You can keep working with your database during the export process as the extraction will be performed in the background.
Note: avoid changing data in tables you have selected to be exported while the exporting is in progress.
In the end you will see status message:
![](images/dt/dt_message-success.png)

## Importing data from CSV format
You can import data from CSV file(s) directly into your database table(s).

1. Select a table(s) to which you want to import data. In the context menu choose "Import Data":
![](images/dt/dt-import-menu.png)

2. Choose import format (CSV):

![](images/dt/dt-import-format.png)

3. Select input CSV file for each table you want to import and you can change the Importer settings (format specific) at this step: 
![](images/dt/dt-import-files.png)

4. Set CSV-to-table mappings. 
You need to set a column in the CSV file for each database table column.
You can skip columns (the value will be set to NULL in the target table column).
You can set constant values for the table column if there is no source column for it in the CSV.
![](images/dt/dt-import-mappings.png)

5. Set options for loading data in the database. These options may affect the loading's performance:
![](images/dt/dt-options-load.png)

About the replacing method option, you can [read here](Data-Import-and-Replace).

6. Review which file(s) and to which table(s) you will import. You can also save all your settings as a task in this step:
![](images/dt/dt-import-final.png)

7. Press finish. See extraction progress. You can keep working with your database during the export process as the data loading will be performed in the background.
Note: avoid changing data in tables you have selected to be imported while the import is in progress.
In the end you will see the status message:
![](images/dt/dt_message-success_import.png)

Related topic: [Migrating table(s) data to another database table(s)](Data-migration)

