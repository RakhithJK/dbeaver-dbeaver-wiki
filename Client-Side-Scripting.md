You can use special commands in the SQL scripts.  
These commands are executed on DBeaver's side, not on the server-side.

DBeaver supports the following commands:

Command | Database | Description |
-----------|-------------|-------------|
`@set var = value` | All | Sets a script variable.<br/> You can use expressions as a value. Variables can be used as SQL queries input parameters.<br/>For more information see [Dynamic parameter bindings](SQL-Execution#dynamic-parameter-bindings)
`@unset var` | All | Unsets a script variable.
`@echo message` | All | Prints message to output log. You can use a macro in a message (for example `${var}`).
`@include fileName` | All | - Executes a specified file name,<br/> - Can be used in scripts, <br/> - Opens a new SQL console with the specified file and processes SQL queries as in a regular SQL editor.
`source fileName` | MySQL | The same as `@include` but in MySQL CLI syntax
`define var = value` | Exasol | The same as `@set` but in Exasol EXAPlus syntax.

