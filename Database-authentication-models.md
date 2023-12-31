DBeaver supports many different authentication models for different databases.
The default authentification model is `native` - it needs a user name and password which are used to authenticate at the remote database server.

Some database drivers support other database-specific authentications.

### PgPass

PostgreSQL specific model. Uses local file PGPASS to obtain user name and/or password.  
It does not have any additional parameters.

Parameter | Description
---|---
Model ID | postgres_pgpass

### Kerberos <img src="images/commercial_big.png" align="top" vspace="2" height="24">

Parameter | Description
---|---
Model ID | krb5, postgresql_krb5, prestodb_krb5, prestosql_krb5, oracle_krb5
krb5.realm | Kerberos realm/AD domain
krb5.kdc_server | KDC server IP/host name
krb5.user | Kerberos user name
krb5.use_keytab | Force keytab file usage (true/false)
krb5.keytab_path | Keytab file path
krb5.use_kinit | Force kinit utulity usage
krb5.kdc_over_tcp | Force TCP/IP protocol usage (UDP is used by default)

### Oracle Wallet <img src="images/commercial_big.png" align="top" vspace="2" height="24">

Oracle Wallet authentication

Parameter | Description
---|---
Model ID | oracle_wallet
oracle.net.wallet_location | Wallet file location

### Oracle OS auth

Oracle native OS authentication

Parameter | Description
---|---
Model ID | oracle_os

### Oracle native database auth

Oracle native database authentication

Parameter | Description
---|---
Model ID | oracle_native


### AWS IAM auth <img src="images/commercial_big.png" align="top" vspace="2" height="24">

AWS IAM authentication

Parameter | Description
---|---
Model ID | iam
iam.region | AWS region ID
iam.aws_access_key | AWS Access Key
iam.aws_secret_key | AWS Secret Key
iam.use_default_aws | Load access/secret key from local AWS configuration
