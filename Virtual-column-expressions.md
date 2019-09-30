## Expression language

You can use standard JavaScript-like expression language. DBeaver uses Jexl engine to process expressions.  
Language reference and examples can be found here: http://commons.apache.org/proper/commons-jexl/reference/syntax.html

## Column values

All columns values in current resultset can be referred by name.
Expression `column1 + column2` will produce sum of two numeric columns or concatenation of two string columns `column` and `column2`.

## Standard functions

Standard functions declared in namespaces.  
You can refer functions in namespaces as variables - `nsName.functionName(parameters`).

### math

You can access all math function as `math.function(parameters)`.  
You can find all supported math functions here: https://docs.oracle.com/cd/E12839_01/apirefs.1111/e12048/functmath.htm

### geo

Function | Parameters | Description
---|---|---
wktPoint|(longitude, latitude)|Produces WKT (geometry) point out of two coordinates. Default SRID is 4326.
wktPoint|(longitude, latitude, srid)|Produces WKT (geometry) point out of two coordinates and SRID
