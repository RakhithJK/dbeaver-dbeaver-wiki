**Note: This feature is available in [Lite](Lite-Edition), [Enterprise](Enterprise-Edition), [Ultimate](Ultimate-Edition) and <a href="https://dbeaver.com/dbeaver-team-edition">Team</a> editions only.**

Databases that support this feature:
- Cockroach
- EnterpiseDB (EDB)
- Fujitsu
- Greenplum
- HANA
- MySQL
- MariaDB
- [Oracle](#oracle)
- PostgreSQL
- PrestoDB
- PrestoSQL (Kerberos can be used with SSL from JKS)
- Redshift
- Teradata
- TimescaleDB
- Yellowbrick
- YugabyteDB

There are a lot of ways to use Kerberos in your database authentication. On this page, you will learn a few of them. This page describes only the part that you need to do on the client machine (the one on which DBeaver is installed), and it is implied that Kerberos KDC and the necessary configuration are already done on the server.

### Possible settings

Setting|Description
---------------|-----------
**Authentication**| 
Username|Name of the user/role in the database
Kerberos User|A Kerberos user represents a unique identity in a Kerberos system to which Kerberos can assign tickets to access the Kerberos-aware services.
Realm|A Kerberos realm is the domain over which a Kerberos authentication server has the authority to authenticate a user, host, or service. A realm name is often, but not always the upper case version of the name of the DNS domain over which it presides.
KDC Server|The hostname of your KDC server. The Kerberos Key Distribution Center (KDC) is a network service that supplies session tickets and temporary session keys to users and computers within an Active Directory domain. The KDC runs on each domain controller as part of the Active Directory Domain Services (AD DS). So the KDC hostname is the hostname of your DC.
Password|The password of your Kerberos user.
**Extra configuration** |
Use keytab|Select this checkbox if you want to use a keytab file on your machine instead of entering a password.
Use kinit|Select this checkbox if you use the kinit tool on your machine. kinit is a tool that obtains and caches an initial ticket-granting ticket for the user. If this checkbox is selected, you will only need to fill in your Kerberos username in most cases.
Custom krb5.conf|Path to your local Kerberos configuration file.
Debug Kerberos Connection|Select this checkbox if you want to see full Kerberos connection information in your [log files](Log-files).

**Important Note** Some settings can be saved in a session cache. If you have changed the settings and it does not help to connect - restart DBeaver.


### Using the keytab file

A keytab is a file containing pairs of Kerberos principals and encrypted keys (which are derived from the Kerberos password). You can use a keytab file to authenticate various remote systems using Kerberos without entering a password. However, when you change your Kerberos password, you will need to recreate all your keytabs.
Keytab files are commonly used to allow scripts to authenticate automatically using Kerberos without requiring human interaction or access to a password stored in a plain-text file. The script can then use the acquired credentials to access files stored on a remote system.
For DBeaver, it means that when you use a keytab file, you still need to provide all of the credentials other than a password.
You can find this setting in the "Extra configuration" section.

![](images/kerberos-keytab.png)

### Using kinit

kinit is a command-line/terminal tool that obtains and caches an initial ticket-granting ticket for the Kerberos user. All of the credentials are provided either in a configuration file or in a command-line interface. This means that to authenticate with kinit in DBeaver, you only need to provide a kerberos username and select this checkbox to use kinit. You can find this setting in the "Extra configuration" section.

![](images/kerberos-kinit.png)

### Using a password

This method is almost the same as using a keytab file, but instead of providing an encrypted file, you must manually enter a password.

![](images/kerberos_pasword.png)

### Extra options

Sometimes you may need to specify the path to the Kerberos configuration file. You can do it in the "Extra configuration" settings section.
You can also specify the path to Kerberos credential cache file near the "Use kinit" checkbox.

![](images/kerberos-config.png)

If your database Kerberos authentication requires the remote coordinator Kerberos service name, add it to the "Service" field.
If SSL on the server is not trusted - you can check the "Use SSL from JKS" setting and manually add a path to your .jks file. A Java keystore (JKS) file is a secure file format used to hold certificate information for Java applications. SSL JKS password can be added in the "SSL JKS" field.
For now, these settings are only available for the PrestoSQL connection.

![](images/kerberos-keystore.png)

### Oracle

Oracle JDBC driver 21 has broken Kerberos authentication, at least for most of the old configurations.  
Use an older driver (12.x or 19.x) in order to use Kerberos authentication in Oracle.  