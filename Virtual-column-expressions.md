## Expression language

You can use standard JavaScript-like expression language. DBeaver uses Jexl engine to process expressions.  
Language reference and examples can be found here: http://commons.apache.org/proper/commons-jexl/reference/syntax.html

## Standard functions

Standard functions declared in namespaces.  
You can refer functions in namespaces as variables (`nsName.functionName(parameters`).

### math

### geo

Function | Parameters | Description
---|---|---
wktPoint|(longitude, latitude)|Produces WKT (geometry) point out of two coordinates. Default SRID is 4326.
wktPoint|(longitude, latitude, srid)|Produces WKT (geometry) point out of two coordinates and SRID
