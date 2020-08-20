DBeaver supports many different authentication models for different databases.
Default auth model is `native` - it need user name and password which are used to authenticate at the remote database server.

Some database drivers support other database-specific authentication.

### PgPass

PostgreSQL specific model. Uses local file PGPASS to obtain user name and/or password.  
It doesn't have any additional parameters.

Parameter | Description
---|---
Model ID | postgres_pgpass
