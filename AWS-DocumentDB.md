
AWS DocumentDB is based on the [[MongoDB]] engine.  
It has several minor differences in the query processing and network configuration.  
However most features which work for MongoDB will work for DocumentDB as well. Please refer to [[MongoDB]] article. 

### Connections

AWS restricts direct access to DocumentDB clusters from outside of the cloud (region). So you can connect to it directly (using cluster host name) only when DBeaver is deployed on the EC2 instance.  

In other cases you will need to use SSH tunnel thru a proxy machine to access DocumentDB instance. Please read AWS Documentation about proxy configuration: https://docs.aws.amazon.com/documentdb/latest/developerguide/connect-from-outside-a-vpc.html

In DBeaver you can use SSH tab on the connection settings page. Just enter proxy host, user name and specify private key file (it is provided by AWS as a keypair).

### Queries

DBeaver processes DocDB SQL queries exactly like in [[MongoDB]]. It supports SELECT, UPDATE, INSERT and DELETE queries.  
SELECT queries support WHERE, ORDER BY, GROUP BY and HAVING clauses.

DocumentDB restricts `eval` function so all JavaScript queries will be parsed on the client side and then evaluated at DocDB cluster one by one.
Most of JS functions works exactly like in Mongo Shell.

