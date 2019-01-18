You can use pre-configured database driver or create new driver.

DBeaver has a lot of pre-configured driver including SQL, NoSQL, key-value databases, graph databases, search engines, etc.
But sometimes you need to connect to a database which was not configured in DBeaver yet.

All you need is JDBC driver of your database the ret is easy.

### Adding new JDBC driver

JDBC driver is a program (in Java) which can connect and operate with some local or remote database server. It usually provides all needed functionality to cover 100% of database functionality. Usually JDBC driver are made by database vendors to let customers ability to work with their databases.

JDBC driver consists of one or multiple `jar` files. Jar file is a library which contains program code and some other files.
You need to download driver's jar files before adding them in DBeaver. Sometimes jar files are included in database server distribution - in that case you need to refer your database documentation or ask your DBA.