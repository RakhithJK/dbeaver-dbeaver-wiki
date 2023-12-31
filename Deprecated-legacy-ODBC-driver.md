The Legacy ODBC driver was removed in DBeaver Community Edition **23.1**.

## Why was it removed?

- DBeaver users have encountered many issues with the outdated ODBC driver related to old drivers, which cannot be fixed by the DBeaver team.
- This ODBC driver is based on the obsolete Java version 7.
- It does not work on Linux and macOS, and that cannot be improved.

## How to connect via ODBC

If you want to connect to the databases via ODBC, you have the following options:

#### 1. Use ODBC driver in PRO versions

The new ODBC JDBC driver developed by the DBeaver team supports most new database drivers, works on Linux and macOS, and will be supported by the DBeaver team. It is available in Lite, Enterprise, Ultimate, and Team editions.

[Learn more about the PRO ODBC driver](ODBC-JDBC-Driver)

#### 2. Download Legacy ODBC from GitHub

This driver is deprecated and not recommended for use because of many issues. It is based on Java 7, which prevents us from improving it. The DBeaver team does not support this driver and is not responsible for its work, but you can use it at your own risk.

[Download the legacy ODBC driver](https://github.com/dbeaver/jdbc-odbc-bridge-jre7)

#### 3. Use a third-party ODBC driver

You can look for another ODBC driver that matches your database and try to use it. Follow this instruction to add a driver in DBeaver and configure it.

[How to add a driver in DBeaver](Database-drivers/#adding-driver-configuration-in-dbeaver)

## How to transfer connections from the old ODBC to the new one in the Community version

If you have been using the legacy ODBC driver in DBeaver Community and have some connections associated with it, you need to do the following:

1. Install the new ODBC driver that you want to use instead of the legacy one ([legacy ODBC from GitHub](#2-download-legacy-odbc-from-github) or [third-party ODBC](#3-use-a-third-party-odbc-driver)). 

2. Re-associate the old connections: select such connections, go to Database -> Change Connection(s) Driver, and find the newly installed ODBC.

Another option is to remove the old connections created with the legacy ODBC driver and create new connections associated with the newly installed ODBC.