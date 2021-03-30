DBeaver supports the following commands:

Command | Database | Description |
-----------|-------------|-------------|
@set&nbsp;var&nbsp;=&nbsp;value | All | Sets a script variable.<br/> You can use expressions as a value. Variables can be used as SQL queries input parameters.
@unset&nbsp;var | All | Unsets a script variable.
@echo&nbsp;message | All | Prints message to output log. You can use a macro in a message (for example ${var}).
@include&nbsp;fileName | All | - Executes a specified file name,<br/> - Can be used in scripts, <br/> - Opens a new SQL console with the specified file and processes SQL queries as in a regular SQL editor.
source&nbsp;fileName | MySQL | The same as @include but in MySQL CLI syntax
define&nbsp;var&nbsp;=&nbsp;value | Exasol | The same as @set but in Exasol EXAPlus syntax.

