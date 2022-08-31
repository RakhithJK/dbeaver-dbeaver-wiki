## Connecting to Oracle databases

There are several ways to configure database connection and several ways to perform authentication.

## Configuration types 

### Basic connections

Host/port based configuration

Parameter | Description | Example
----|-----|----
Host | Server host name | 192.168.1.25
Post number | Server listener port | 1521 (default)
Database | Service or SID name | ORCL
Service/SID | It depends on server configuration. SID must be selected for some servers and Service Name for others | SID

### TNS connections

TNS configuration is the simplest but it requires you to have `tnsnames.ora` file somewhere on disk.
tnsnames.ora contains information about all accessible Oracle server connections.
DBeaver can determine default location of this file but sometimes you need to specify it manually

Parameter | Description | Example
----|-----|----
Network Alias | Name of configuration from tnsnames.ora | ORCL1
TNS names path | Path to `tnsnames.ora` file. By default it is get from TNS_ADMIN environment variable or from Windows registry | c:\oracle\network\admin


### Custom URL

## Authentication

### Database

### OS authentication

### Kerberos

### Oracle Wallet

## Oracle Cloud connections