**Note: Cassandra extension is available only in [[Enterprise-Edition]] version.**

### Browsing Cassandra tables

You can browse, view, edit and filter Cassandra tables the same way as with regular (relational) tables.
However, being a distributed key-value database, Cassandra doesn't support any kind of referential integrity. There are no foreign keys, references, etc.
Note that Cassandra has very advanced (comparing to relational databases) data type system. Each column may be a collection, map or set of values (with very big number of values). In some cases this makes browsing data in the "Grid" mode inconvenient.

### Executing CQL

CQL (Cassandra Query Language) is a kind of very simple SQL language dialect. It supports simple SELECT queries, DDL statements (like CREATE TABLE) and some other.
http://cassandra.apache.org/doc/4.0/cql/
You can use standard DBeaver SQL editor to execute CQL queries.

### ERD

Physical ERD (Entity Relation Diagram) doesn't make much sense for Cassandra as there are no any foreign keys.
However you can make you own [custom ERD](Custom-Diagrams) and connect actual Cassandra table with each other using logical associations.
