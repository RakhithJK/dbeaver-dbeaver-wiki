In some cases custom JDBC drivers work incorrectly in DBeaver - shows wrong metadata like table columns, constraints or foreign keys.  
Usually it happens because driver isn't compliant with JDBC API specification and DBeaver can't correctly interpret metadata provided by driver.

To understand what is going on inside driver you can enable JDBC tracing:

1. Find `dbeaver.ini` file (it is located in the same folder where DBeaver is installed)
1. Add line `-Ddbeaver.jdbc.trace=true` in the end of `dbeaver.ini`
1. Restart DBeaver
1. Connect to your database and browse metadata in the database navigator/object editors.
1. In DBeaver [[Workspace|Workspace-Location]] go to `.metadata` folder
1. File `jdbc-api-trace.log` contains all JDBC API invocations and all queries with results.

Analyzing contents of `jdbc-api-trace.log` you can understand what is wrong with metadata. Attach piece of trace file in GitHub ticket if you think that something is wrong on DBeaver side.

WARNING: disable JDBC tracing in your regular work. Enable it only for debugging. Trace generation decreases application performance and may produce huge log files.
