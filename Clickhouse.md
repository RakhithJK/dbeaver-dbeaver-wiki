### Yandex Clickhouse

<a href="https://clickhouse.yandex/docs/en/">ClickHouse</a> is an open source column-oriented database management system capable of real time generation of analytical data reports using SQL queries.

DBeaver uses standard Clickhouse JDBC driver to communicate with Clickhouse servers. Driver is downloaded automatically once you establish connection with database server.

### Connection setup

Connection initiation is very easy.

1. Select Clickhouse driver:

![](images/database/clickhouse/clickhouse-setup-driver.png)

2. The only required connection parameter is host name.

![](images/database/clickhouse/clickhouse-setup-connection.png)

3. You can configure SSH tunnel to access your server. In that case set database host name to `localhost` while real Clickhouse server host will be specified as SSH server.

![](images/database/clickhouse/clickhouse-setup-ssh.png)

4. Test connection:

![](images/database/clickhouse/clickhouse-test-connection.png)

### Schema/data browser

You can browse/edit, analyse data in Clickhouse tables:

![](images/database/clickhouse/clickhouse-tables.png)

DBeaver supports native Clickhouse table DDLs:

![](images/database/clickhouse/clickhouse-ddl.png)

Clickhouse extension support most of standard DBeaver features (SQL editor, data view/edit, data transfer, mock data generation, etc).

#### Limitations

Clickhouse doesn't support referential integrity so you won't see foreign keys. ER diagrams are also doesn't make much sense.
