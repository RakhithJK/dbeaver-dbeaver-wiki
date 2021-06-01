### Yandex Clickhouse

<a href="https://clickhouse.yandex/docs/en/">ClickHouse</a> is an open source column-oriented database management system capable of real time generation of analytical data reports using SQL queries.

DBeaver uses a standard Clickhouse JDBC driver to communicate with Clickhouse servers. The driver is downloaded automatically once you establish a connection with the database server.

### Connection setup

Connection initiation is very easy.

1. Select Clickhouse driver:

![](images/database/clickhouse/clickhouse-setup-driver.png)

2. The only required connection parameter is the host name.

![](images/database/clickhouse/clickhouse-setup-connection.png)

3. You can a configure SSH tunnel to access your server. In this case, set the database host name to `localhost` while the real Clickhouse server host will be specified as an SSH server.

![](images/database/clickhouse/clickhouse-setup-ssh.png)

4. Test connection:

![](images/database/clickhouse/clickhouse-test-connection.png)

### Schema/data browser

You can browse/edit, analyse data in Clickhouse tables:

![](images/database/clickhouse/clickhouse-tables.png)

DBeaver supports native Clickhouse table DDLs:

![](images/database/clickhouse/clickhouse-ddl.png)

Clickhouse extension supports most standard DBeaver features (SQL editor, data view/edit, data transfer, mock data generation, etc).

#### Limitations

Clickhouse does not support referential integrity so you will not see foreign keys. ER diagrams are also does not make much sense.
