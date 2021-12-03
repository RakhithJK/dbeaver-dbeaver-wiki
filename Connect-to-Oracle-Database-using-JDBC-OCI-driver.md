In this article, we discuss a way to establish connections to an Oracle database using JDBC OCI (Type II). 
Please take into consideration that the proposed way uses DBeaver's Generic driver. 
This means that you cannot get Oracle-specific functionality this way.

## Prerequisites

JDBC OCI connections require 
[Oracle Instant Client](https://www.oracle.com/database/technologies/instant-client/downloads.html) 
on the local machine. Please pay attention to the versions of the Instant Client and the JDBC driver, 
as they must be identical. Currently, DBeaver uses the 12.2.0.1 version by default, 
so we recommend using the 12.2.0.1 version of the Instant Client.

Install the Instant Client into some folder. We will refer to this folder as ORA_HOME for the rest of the article.
Append ORA_HOME to the PATH variable and restart DBeaver before proceeding.

## Configuration
1. Place your _tnsnames.ora_ file into ORA_HOME/network/admin directory.
2. In DBeaver, click Window -> Driver Manager -> New. This opens Create new driver dialog.
3. In the Settings tab, add a _Driver name_ of your liking. Set _Class Name_ to 'oracle.jdbc.OracleDriver'.
Set URL Template to 'jdbc:oracle:oci:@tnsAlias', where 'tnsAlias' is alias from your _tnsnames.ora_ file.
Make sure that the Driver Type is set to Generic.
4. In the Libraries tab, you need to add Maven artifacts. To do that, click Add Artifact. Paste the following XML into
the text field:

```XML
<dependencies>
    <dependency>
        <groupId>com.oracle.database.jdbc</groupId>
        <artifactId>ojdbc8</artifactId>
        <version>12.2.0.1</version>
    </dependency>
    <dependency>
        <groupId>com.oracle.database.nls</groupId>
        <artifactId>orai18n</artifactId>
        <version>12.2.0.1</version>
    </dependency>
    <dependency>
        <groupId>com.oracle.database.xml</groupId>
        <artifactId>xdb6</artifactId>
        <version>12.2.0.1</version>
    </dependency>
    <dependency>
        <groupId>com.oracle.database.xml</groupId>
        <artifactId>xmlparserv2</artifactId>
        <version>12.2.0.1</version>
    </dependency>
</dependencies>
```
**NB:** Replace the versions of the artifacts if you use a different version of the Instant Client.

5. In the Driver properties tab, make right-click -> Add new property. 
6. Set the property name to 'protocol' (without quotes). Set the Value to 'oci' (without quotes).
7. Close the Driver manager.
8. Create a new connection using your newly configured driver.
