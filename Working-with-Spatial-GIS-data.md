## Spatial data

Spatial data is geometry or geography value which can be represented on a map or as a graph. Geometry object consists from a series of points. <a href="https://en.wikipedia.org/wiki/Spatial_database">More details</a>.

## Spatial data viewer

![](images/ug/Data-view-gis.png)
![](images/ug/Data-view-gis-presentation.png)

## Converting longitude/latitude to geography points

Generally any combination of longitude/latitude (as float point numbers) can be represented as geometry value.

## Supported databases

- PostgreSQL (PostGIS)
- MySQL
- SQLite (GeoPackage)
- H2GIS
- SAP HANA
- Oracle <img src="images/ee.png" vspace="0" border="0" height="18"/>
- SQL Server <img src="images/ee.png" vspace="0" border="0" height="18"/>

## Viewing string or binary data on a map 

You can also see your geodata on the map if you select the data cell setting "View/Format", then "Set columnName format" and among the formats - Geometry. 
This works for both string and binary type of columns.

![](images/ug/Data-view-gis-string-to-spatial.png)
String column type to spatial.

![](images/ug/Data-view-gis-binary-to-spatial.png)
Binary column type to spatial.
