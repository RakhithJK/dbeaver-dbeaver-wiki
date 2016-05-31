### Open New Connection wizard
If you run DBeaver for the first time (standalone version) then new connection wizard will appear automatically.
Otherwise click on "New Connection" item in the main toolbar or in the Database Navigator view toolbar or in the main menu "Database".
[[images/connect-wizard-item.png]]

#### Choose a driver for your new connection
[[images/connect-wizard-driver.png]]  
To quickly find needed driver you may type a hint in the top text field.  
If you can't find a driver for your database then maybe you need to create a new one.  
Refer to [[Create database driver|Create-database-driver]] article.  

#### Configuring connection
[[images/connect-wizard-settings.png]]  
Set all primary connection properties.
For most drivers required fields are:
- host
- port
- database name 
- user name and password

However number and type of connection properties are very dependent on driver.
Embedded drivers requires only the path to a database.

#### Finish
On the final page you may set connection name, type and initial settings (such as bootstrap queries, transaction state, global filters, etc).
[[images/connect-wizard-general.png]]  

#### Extra configuration
For advanced users.

##### Driver properties
Each driver has it's own set of additional properties. Refer to the driver documentation to get information about available properties and their values.  
[[images/connect-wizard-settings-driver.png]]  

##### Network settings (SSH, SOCKS, SSL)
If your database cannot be accessed directly you can use SSH tunnel.  
[[images/connect-wizard-ssh.png]]  