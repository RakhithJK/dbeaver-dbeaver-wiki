## Connecting to Oracle databases

There are several ways to configure database connection and several ways to perform authentication.

![](images/database/oracle/connection-page.png)

## Configuration types 

### Basic connections

Host/port based configuration

Parameter | Description | Example
----|-----|----
Host | Server host name | 192.168.1.25
Post number | Server listener port | 1521 (default)
Database | Service or SID name | ORCL
Service/SID | It depends on server configuration.<br/>SID must be selected for some servers and Service Name for others | SID

### TNS connections

TNS configuration is the simplest but it requires you to have `tnsnames.ora` file somewhere on disk.
tnsnames.ora contains information about all accessible Oracle server connections.
DBeaver can determine default location of this file but sometimes you need to specify it manually

Parameter | Description | Example
----|-----|----
Network Alias | Name of configuration from tnsnames.ora | ORCL1
TNS names path | Path to `tnsnames.ora` file.<br/> By default it is get from TNS_ADMIN environment variable or from Windows registry | c:\oracle\network\admin

### Custom URL

For more sophisticated configuration you can specify full JDBC URL manually (see [Data Sources and URLs](https://docs.oracle.com/database/121/JJDBC/urls.htm#JJDBC28270)). 

Sample URL (Oracle Cloud):  
`jdbc:oracle:thin:@(description= (retry_count=20)(retry_delay=3)(address=(protocol=tcps)(port=1522)(host=adb.us-ashburn-1.oraclecloud.com))(connect_data=(service_name=xxxxxxxxxxxxxxxxx_high.adb.oraclecloud.com))(security=(ssl_server_cert_dn="CN=adwc.uscom-east-1.oraclecloud.com, OU=Oracle BMCS US, O=Oracle Corporation, L=Redwood City, ST=California, C=US")))`

## Authentication

### Database

### OS authentication

### Kerberos

### Oracle Wallet

## Oracle Cloud connections