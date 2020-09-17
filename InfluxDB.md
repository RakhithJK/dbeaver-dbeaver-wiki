### Overview

DBeaver EE supports InfluxDB schema browser, data viewer and InfluxQL queries execution.  
DBeaver uses InfluxDB Java driver 2.12 to operate with the server over HTTP/HTTPS (standard InfluxDB protocol).  
It supports InflixDB servers of any version (in the moment of writing).  

### Connecting to Influx Server

You can connect directly to a server or use SSH tunneling or SOCKS proxy.  

![](images/database/influxdb/influxdb-connection-init.png)

![](images/database/influxdb/influxdb-connection-ssh.png)

### Browsing InfluxDB schema

InfluxDB is <a href="https://docs.influxdata.com/influxdb/v1.6/concepts/crosswalk/">TimeSeries database</a>, it doesn't support tables, foreign keys and other relational entities.</p>
DBeaver doesn't support data insert/update in InfluxDB. Basically for DBeaver database is in read-only state. You can browse schema and view/analyse data.  
While data itself is loaded by various sensors/data collectors in real time.  
Instead of tables InfluxDB has <a href="https://docs.influxdata.com/influxdb/v1.6/concepts/key_concepts/#measurement">measurements</a>. Instead of columns it has <a href="https://docs.influxdata.com/influxdb/v1.6/concepts/key_concepts/#field-key">fields</a> and <a href="https://docs.influxdata.com/influxdb/v1.6/concepts/key_concepts/#tag-key">tags</a>.  

![](images/database/influxdb/inflixdb-schema.png)

### Executing InfluxQL
<a href="https://docs.influxdata.com/influxdb/v1.6/query_language/">InfluxQL</a> is a query language similar to SQL.  
DBeaver fully supports all InfluxQL statements. Query results are presented as grid or as graphs:  

![](images/database/influxdb/inflixdb-ql.png)
![](images/database/influxdb/inflixdb-ql2.png)