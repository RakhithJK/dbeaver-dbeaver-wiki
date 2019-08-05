### Configure drivers with pre-installed jars

You can customize drivers configuration in [[workspace|Workspace-Location]]/.metadata/.plugins/org.jkiss.dbeaver.core/drivers.xml file.
If you have some pre-installed jar files you can reference them in drivers.xml. 
Example:
```xml
<library type="jar" path="absolute-jar-folder-path\driver-jar.jar" custom="true"/>
```
Also in drivers.xml you can use following variables to specify relative paths:

Variable | Meaning 
-----------|-------------
drivers_home | Standard DBeaver drivers location - ($workspace/drivers by default)
dbeaver_home | DBeaver installation folder
home | User home folder
workspace | DBeaver workspace path

For instance: 
```xml
<library type="jar" path="${workspace}\drivers\my-driver.jar" custom="true"/>
```

Full drivers.xml example:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<drivers>

	<provider id="postgresql">
		<driver id="postgres-jdbc" custom="false" embedded="false" name="PostgreSQL" class="org.postgresql.Driver" url="jdbc:postgresql://{host}[:{port}]/[{database}]" port="5432" description="PostgreSQL standard driver">
			<library type="jar" path="maven:/org.postgresql:postgresql:RELEASE" custom="false" version="42.2.3">
				<file id="org.postgresql:postgresql" version="42.2.3" path="${drivers_home}/maven/maven-central/org.postgresql/postgresql-42.2.3.jar"/>
			</library>
			<library type="jar" path="maven:/net.postgis:postgis-jdbc:RELEASE" custom="false" version="2.2.1">
				<file id="net.postgis:postgis-jdbc" version="2.2.1" path="${drivers_home}/maven/maven-central/net.postgis/postgis-jdbc-2.2.1.jar"/>
			</library>
			<library type="jar" path="maven:/net.postgis:postgis-jdbc-jtsparser:RELEASE" custom="false" version="2.2.1">
				<file id="net.postgis:postgis-jdbc-jtsparser" version="2.2.1" path="${drivers_home}/maven/maven-central/net.postgis/postgis-jdbc-jtsparser-2.2.1.jar"/>
			</library>
		</driver>
	</provider>
	
</drivers>
```