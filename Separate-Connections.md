By default, DBeaver creates separate connections for SQL Editor and Metadata read for most databases except these:
- SQLServer Azure AD MFA
- BigQuery
- BigTable
- Spanner
- Apache Hadoop, Apache Drill, Apache Kyuubi, Apache Spark, Apache Hive, SnappyData, Gemfire XD, Apache Phoenix
- Redshift
- Snowflake

Opening separate metadata connection may increase performance because there will be no UI locks during query execution.

You can set up opening separate connection for metadata read globally in Preferences->Connections->Metadata or per each connection in Connection configuration->Metadata.

![](images/separate-connection-meta.png)

Opening separate connection for SQL Editor may allow you to have different execution context for each script.

You can set up opening separate connection for each editor in Preferences->Editors->SQL Editor and Connection configuration->SQL Editor and Connection configuration->SQL Editor.

![](images/separate-connection-editor.png)