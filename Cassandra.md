**Note: Cassandra extension is available only in [Enterprise Edition](Enterprise-Edition) version.**

### Overview 
DBeaver EE supports Cassandra schema browser, data viewer and CQL queries execution.
Also it supports various administrative tools.

### Connecting to Cassandra cluster

You can connect directly to a server or use SSH tunneling or SOCKS proxy.
DBeaver uses DataStax Java driver to operate with server. It supports Cassandra servers 2.x, 3.x or higher.  

![](images/database/cassandra/cassandra-connection-init.png)
![](images/database/cassandra/cassandra-connection-ssh.png)
![](images/database/cassandra/cassandra-connection-ssl.png)
![](images/database/cassandra/cassandra-connection-tcp.png)

### Browsing Cassandra tables

You can browse, view, edit and filter Cassandra tables the same way as with regular (relational) tables.
However, being a distributed key-value database, Cassandra doesn't support any kind of referential integrity. There are no foreign keys, references, etc.  
Note that Cassandra has very advanced (comparing to relational databases) data type system. Each column may be a collection, map or set of values (with very big number of values). In some cases this makes browsing data in the "Grid" mode inconvenient.

![](images/database/cassandra/cassandra-schema.png)
![](images/database/cassandra/cassandra-data-grid.png)

### Executing CQL

CQL [[Cassandra Query Language|http://cassandra.apache.org/doc/4.0/cql/]] is a kind of very simple SQL language dialect.  
It supports simple SELECT queries, DDL statements (like CREATE TABLE) and some other.

You can use standard DBeaver SQL editor to execute CQL queries.
DBeaver supports Cassandra query execution, results scrolling, data export/import, mock data generation and other features.
Data viewer (of individual tables or custom CQL query results) query tracing is supported.  

![](images/database/cassandra/cassandra-cql-trace.png)

### ERD

Physical ERD (Entity Relation Diagram) doesn't make much sense for Cassandra as there are no any foreign keys.
However you can make you own [custom ERD](Custom-Diagrams) and connect actual Cassandra table with each other using logical associations.
