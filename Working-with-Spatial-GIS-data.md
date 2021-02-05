Spatial data is a geometry or geography value that can be represented on a map or as a graph. Geometry object consists from a series of points. <a href="https://en.wikipedia.org/wiki/Spatial_database">More details</a>.

DBeaver's support of spatial data covers the following databases:
- PostgreSQL (PostGIS)
- MySQL
- SQLite (GeoPackage)
- H2GIS
- SAP HANA
- Oracle <img src="images/ee.png" vspace="0" border="0" height="18"/>
- SQL Server <img src="images/ee.png" vspace="0" border="0" height="18"/>

## Spatial data viewer

![](images/ug/Data-view-gis.png)
![](images/ug/Data-view-gis-presentation.png)

### Tile layer management
_Will be written soon._
### Defining custom tile layer
_Feature is under active development and will be out with version 7.3.5. Stay tuned._
## Viewing string or binary data on a map 

You can also see your geodata on the map if you select the data cell setting "View/Format", then "Set columnName format" and among the formats - Geometry. 
This works for both string and binary types of columns.

![](images/ug/Data-view-gis-string-to-spatial.png)
String column type to spatial.

![](images/ug/Data-view-gis-binary-to-spatial.png)
Binary column type to spatial.