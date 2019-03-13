### SQL Queries

PostgreSQL queries reading GIS data types: (can be executed in SQL editor)
```sql
SELECT ST_MakePoint(112.123,243.123);

SELECT GeomFromEWKT('SRID=4326;POINT(111.1111111 1.1111111)');

SELECT GeomFromEWKT('SRID=4326;POLYGON((0 0,0 1,1 1,1 0,0 0))');
```

### Test databases

https://knowledge.safe.com/questions/70649/fme-basic-training-postgis-database-connection.html