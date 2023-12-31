DBeaver can change credentials for the current database user. 

Databases that support this feature:
- PostgreSQL
- Greenplum
- Cockroach
- Redshift <img src="images/commercial.png" vspace="4" align="top"/>
- Netezza <img src="images/commercial.png" vspace="4" align="top"/>
- SQL Server
- Oracle
- Exasol
- Snowflake <img src="images/commercial.png" vspace="4" align="top"/>
- Vertica

### Changing expired user password

Different databases perform password management for users in different ways. For some of them, you can change the user password after the expiration date. It works for Oracle, PostgreSQL, and Netezza databases.

For the rest, database users must change the password before the expiration. Otherwise, it will be impossible to do it in DBeaver.

### How to change the user password

You can change the current user password in the Navigation Tree according to the instructions below:

1. Connect to the database.
2. Open the context menu by right-clicking on the connection in the Navigation tree.
3. Select a "Security" point and click on a "Change user password" point in a sub-menu.

![](images/ug/Connection-Security-Change.png)

4. When a new password input dialog opens, enter and confirm the new password.

![](images/ug/Change-User-Password-Dialog.png)

5. Confirm the password changes. 
(This dialog will not appear if the entered password is incorrect).

![](images/ug/Change-User-Password-Save-Settings.png)

The password has been changed.
