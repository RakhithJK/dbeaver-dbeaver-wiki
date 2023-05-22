The level of security is one of the key questions for enterprises, and the DBeaver team pays a lot of attention to it. One of the best reasons to use PRO versions is to take advantage of its security tools and features, such as password protection, SSO authentication, teams and roles in Team Edition.

This article briefly describes the most important security options available in DBeaver PRO.

- [Changing database password](#changing-database-password)
- [Password protection for Projects](#password-protection-for-projects)
- [Secure authentication](#secure-authentication)
- [Predefined connections](#predefined-connections)
- [User roles and permissions](#users-roles-and-permissions)
- [Centralized updates](#centralized-automatic-updates)
- [License management](#license-management)


## Changing database password

Users can change the current database password directly in DBeaver in the following databases: Cockroach, Exasol, Greenplum, Netezza, Oracle, PostgreSQL, Redshift, Snowflake, SQL Server, and Vertica.

Oracle, PostgreSQL, and Netezza allow changing an expired password in DBeaver as well.

- [How to change the user password](https://dbeaver.com/docs/wiki/Change-current-user-password/)

## Password protection for Projects

### Master password for all your Projects

You can protect all [Projects](https://dbeaver.com/docs/wiki/Projects-View/) in your local workspace with a master password. This feature is only available in DBeaver PRO versions.

You can set this password and store it in DBeaver password provider or use a generated password from your local password provider (for instance, OS X Keystore Integration or Windows integration provider).

[Learn more about master pasword](
https://github.com/dbeaver/dbeaver/wiki/Project-security#master-password-for-local-configuration)

### Password for one project

You can specify a password for any project to protect all the project's configurations. This feature is only available in DBeaver PRO versions.

[Learn more about project pasword](https://github.com/dbeaver/dbeaver/wiki/Project-security#project-password)

## Secure authentication

In DBeaver PRO versions, you can connect to databases using secure authentication via Kerberos or GCP, AWS, and Azure cloud services.

### Kerberos support

Kerberos is an authentication protocol, the default authentication technology used in Microsoft Windows.

You can connect via Kerberos using keytab, kinit, or a password. Open the connection settings, choose one of the [supported databases](Kerberos-Authentication) and select Kerberos as the authentication method.

[Learn more about authentication via Kerberos](Kerberos-Authentication)

### SSO authentication

Users can connect to all company services using only one login and password. This is possible if you use SSO - Single Sign-On authentication service.

You do not need to manage, store, and transfer user credentials. When a user connects to the database, DBeaver opens a web browser with SSO authentication.

DBeaver supports the following SSO authentication services:
- [AWS SSO](https://dbeaver.com/docs/wiki/AWS-SSO/)
- [GCP SSO](https://dbeaver.com/docs/wiki/GCP-SSO/)
- [Azure](https://github.com/dbeaver/dbeaver/wiki/Azure-Cloud-Explorer)

## Predefined connections

### Connections import

You can describe all available database connections in [configuration files](https://dbeaver.com/docs/wiki/Admin-Manage-Connections/#provide-predefined-connections) (in JSON format) or [import from CSV or XML](https://dbeaver.com/docs/wiki/Admin-Manage-Connections/#importing-connections-from-csv-xml) DBeaver.

### Read-only connections

If you want to restrict users from editing connection parameters, you can [protect them with passwords](https://dbeaver.com/docs/wiki/Admin-Manage-Connections/#secure-connections-from-editing).

## Users roles and permissions

### Configuring preferences

You can customize users preferences before they run DBeaver. For example, you can set the default [simple mode](https://dbeaver.com/docs/wiki/Simple-and-Advanced-View/) for all connections (to show only schemas and tables and hide all system and service objects).

[How to manage preferences](https://dbeaver.com/docs/wiki/Admin-Manage-Preferences/#configuring-default-navigator-view-for-new-connections)

### Roles in Team Edition

The best way to manage user access, restrictions, and permissions is to use  [Team Edition](https://dbeaver.com/dbeaver-team-edition/).

Team Edition allows you to create users and assign them appropriate roles with predefined capabilities.

You can add Viewers and Editors to work with prepared data, Managers to prepare data for them, Developers to work with scripts and connections, and administrators to manage everything.

[Learn more about Team Edition](https://dbeaver.com/dbeaver-team-edition/)


## Centralized automatic updates

If your team works on Microsoft Windows, you can organize DBevaer mass updates in silent mode, without user input, using the Windows Installer command line options.

[Learn more about silent install](https://github.com/dbeaver/dbeaver/wiki/Windows-Silent-Install)

## License management

You can place the license file in the user's workspace or store it elsewhere, and specify the license path on the command line or in the DBeaver configuration file.

- [Learn more about lisense management automation](https://dbeaver.com/docs/wiki/License-Administration/#license-management-automation)
- [How to specify license path in config](https://dbeaver.com/docs/wiki/License-Administration/#passing-license-file-through-command-line)
