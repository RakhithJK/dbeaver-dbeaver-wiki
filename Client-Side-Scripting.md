You can use special commands in the SQL scripts.  
These commands are executed on DBeaver's side, not on the server-side.

DBeaver supports the following commands:

Command | Database | Description |
-----------|-------------|-------------|
`@set var = value` | All | Sets a script variable.<br/> You can use expressions as a value. Variables can be used as SQL queries input parameters.<br/>For more information see [Dynamic parameter bindings](SQL-Execution#dynamic-parameter-bindings)
`@unset var` | All | Unsets a script variable.
`@echo message` | All | Prints message to output log. You can use a macro in a message (for example `${var}`).
`@include fileName` | All | - Executes a specified file name,<br/> - Can be used in scripts, <br/> - Opens a new SQL console with the specified file and processes SQL queries as in a regular SQL editor.
`@export { ... }` | All | Opens the data transfer wizard with predefined settings.<br>For more information see [the main section](#Export-command).
`source fileName` | MySQL | The same as `@include` but in MySQL CLI syntax
`define var = value` | Exasol | The same as `@set` but in Exasol EXAPlus syntax.

## Export command

The `@export` command allows you to open the data transfer wizard with prefilled settings.

This article describes supported settings by that command, their purpose and allowed values.
Generally, this article reflects everything that is accessible in the data transfer wizard.
Settings are written in the order they appear in the wizard, so you can always look at the wizard to quickly locate any of settings.

The body of the command consists of JSON which looks like this:

```json
{
    "type": <ID of the processor>,
    "producer": {
        <producer-specific settings>
    },
    "consumer": {
        <consumer settings>
    },
    "processor": {
        <processor settings>
    },
}
```

Due to certain limitations, it must be written on a single line, without line delimiters:

```json
@export { "type": "csv", "producer": { ... }, "consumer": { ... }, "processor": { ... } }
```

Here's the description of each attribute:

|Attribute|Description|
|---|---|
|`type`|Type of the processor.|
|`producer`|Settings that affect how the data is extracted.<br>See the full table of supported settings in [the main section](#Producer-Settings).|
|`consumer`|Settings that affect how the data is transformed before processing.<br>See the full table of supported settings in [the main section](#Consumer-Settings).|
|`processor`|Settings that are specific to the chosen processor by the `type` attribute.<br>See the full table of supported processors in [the main section](#Processor-Settings).|

### Producer Settings

|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`extractType`|Extract type|*Need clarification*|String|`SINGLE_QUERY`|`SINGLE_QUERY`, `SEGMENTS`|
|`segmentSize`|Segment size|*Need clarification*|Integer|`100000`|*Any*|
|`fetchSize`|Fetch size|Number of rows to fetch per one server round trip.<br>May greatly affect extraction performance.|Integer|`10000`|*Any*|
|`openNewConnections`|Open new connection(s)|Open new physical connection for data reading.<br>Makes great sense if you are going to continue to work with your database during export process.|Boolean|`true`|*Any*|
|`queryRowCount`|Select row count|Query row count before performing export.<br>This will let you to track export progress but may cause performance faults in some cases.|Boolean|`true`|*Any*|

### Consumer Settings

|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`formatterProfile`|Formatting Profile|Specifies the profile used for formatting data.|String|&lt;empty&gt;|*Any*|
|`valueFormat`|Value Formatting|Specifies how the data is interpreted.|String|`UI`|`UI`, `EDIT`, `NATIVE`|
|`lobExtractType`|Binaries Policy|Specifies how binaries are processed.|String|`INLINE`|`SKIP`, `FILES`, `INLINE`|
|`lobEncoding`|Binaries Encoding|Specifies how binaries are encoded.|String|`BINARY`|`BASE64`, `HEX`, `BINARY`, `NATIVE`|
|`outputClipboard`|Copy to Clipboard|Specifies that the data should be copied to the clipboard rather written to files on a disk.|Boolean|`false`|*Any*|
|`outputFolder`|Output Directory|Output directory pattern. Specifies there the output files should be located.<br>|String|N/A|*Any*|
|`outputFilePattern`|Output Filename|Output filename pattern.|String|`${table}_${timestamp}`|*Any*|
|`outputEncoding`|Output Encoding|Specifies the file encoding.|String|`UTF-8`|*Any*|
|`outputEncodingBOM`|Insert BOM|Specifies whether the byte order mark should be written to the output file.<br>Common for encoding such as `UTF-16LE`, `UTF-16BE`, `UTF-32LE`, and `UTF-32LE`.|Boolean|`false`|*Any*|
|`outputTimestampPattern`|Timestamp Pattern|Pattern used for the `${timestamp}` variable in `outputFolder` and `outputFilePattern`.|String|`yyyyMMddHHmm`|*Any*|
|`appendToFile`|Append to the end of the file|If file already exists, appends data at end of it.<br>Only works against compatible processors.|Boolean|`false`|*Any*|
|`useSingleFile`|Write to the single file|Write all streams to the single file.<br>Only works against compatible processors.|Boolean|`false`|*Any*|
|`compressResults`|Compress|Specifies whether the output file should be compressed using ZIP.|Boolean|`false`|*Any*|
|`splitOutFiles`|Split output file|Specifies whether the output file should be split using the `maxOutFileSize` threshold. If size exceeds this threshold, a separate file is created and so on.|Boolean|`false`|*Any*|
|`maxOutFileSize`|Maximum file size|Maximum size of a single file.<br>See `splitOutFiles`|Integer|10000000|*Any*|
|`mappings`|Column mappings|Mappings of the columns. Allows to skip certain columns.|Object|*TBD*|*TBD*|
|`eventProcessors`|Event processors|Special processors that are invoked after the transfer is finished.|*TBD*|*TBD*|*Any*|

### Processor Settings

#### CSV (`csv`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`extension`|File extension|&nbsp;|String|`csv`|*Any*|
|`delimiter`|Delimiter|Column delimiter. You can use special characters \ + t,n,r|String|`,`|*Any*|
|`rowDelimiter`|Row delimiter|Row delimiter. Default is system-specific line feed delimiter. You can use special characters \ + t,n,r|String|`default`|`default`, `\n`, `\r`, `\r\n`, `\n\r`|
|`header`|Header|CSV header settings|String|`top`|`none`, `top`, `bottom`|
|`headerFormat`|Header format|Header format|String|`label`|`label`, `description`, `both`|
|`escape`|Characters escape|Bad characters escaping model (surrounded with quotes or escaped with '\' character)|String|`quotes`|`quotes`, `escape`|
|`quoteChar`|Quote character|Character which will be used to quote strings (space means no quote)|String|`"`|*Any*|
|`quoteAlways`|Quote always|Quote all cell values. Cannot be used with "quoteNever"|String|`disabled`|`disabled`, `all`, `strings`, `all but numbers`, `all but nulls`|
|`quoteNever`|Quote never|Do not quote cell values. Cannot be used with "quoteAlways"|Boolean|`false`|*Any*|
|`nullString`|NULL string|String which will be used instead of NULL values|String|*&lt;empty&gt;*|*Any*|
|`formatNumbers`|Format numbers|Format numeric values using locale settings|Boolean|`false`|*Any*|

#### DbUnit (`dbunit`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`upperCaseTableName`|Force upper case table name|&nbsp;|Boolean|`true`|*Any*|
|`upperCaseColumnNames`|Force upper case column names|&nbsp;|Boolean|`true`|*Any*|
|`extension`|File extension|&nbsp;|String|`xml`|*Any*|
|`includeNullValues`|Include NULL values in export |&nbsp;|Boolean|`true`|*Any*|
|`nullValueString`|Replace NULL values with|&nbsp;|String|`[NULL]`|*Any*|

#### HTML (`html`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`extension`|File extension|&nbsp;|String|`html`|*Any*|
|`tableHeader`|Output table header|Output query or table name as first row in generated table|Boolean|`true`|*Any*|
|`columnHeaders`|Output column headers|Output column names as extra row in generated table|Boolean|`true`|*Any*|
|`extractImages`|Images|Extract images to graphic files|Boolean|`true`|*Any*|

#### JSON (`json`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`printTableName`|Print table name|&nbsp;|Boolean|`true`|*Any*|
|`formatDateISO`|Format dates in ISO 8601|&nbsp;|Boolean|`true`|*Any*|
|`extension`|File extension|&nbsp;|String|`json`|*Any*|

#### Markdown (`markdown.table`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`extension`|File extension|&nbsp;|String|`md`|*Any*|
|`nullString`|NULL string|String which will be used instead of NULL values|String|*&lt;empty&gt;*|*Any*|
|`formatNumbers`|Format numbers|Format numeric values using locale settings|Boolean|`false`|*Any*|
|`showHeaderSeparator`|Show header separator|Print header separator (---). Required for GitHub markdown.|Boolean|`true`|*Any*|
|`confluenceFormat`|Confluence format|Use Confluence format (special format of header and no separator line)|Boolean|`false`|*Any*|

#### SQL (`sql`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`includeAutoGenerated`|Include generated columns|Include auto-generated columns (e.g. auto-increment) in SQL INSERT|Boolean|`false`|*Any*|
|`extension`|File extension|&nbsp;|String|`sql`|*Any*|
|`nativeFormat`|Native date/time format|Use native date/time format in INSERT statements|Boolean|`true`|*Any*|
|`omitSchema`|Omit schema name|Omit schema/catalog name in INSERT statements|Boolean|`false`|*Any*|
|`rowsInStatement`|Data rows per statement|Number of data rows per single insert statement|Integer|`10`|*Any*|
|`lineBeforeRows`|Insert line before rows|Insert line feed before values (for multi-row inserts)|Boolean|`true`|*Any*|
|`keywordCase`|Keyword case|You can choose lower or upper keyword case|String|`upper`|`upper`, `lower`|
|`identifierCase`|Identifier case|You can choose lower or upper keyword case for table and column names|String|`as is`|`as is`, `upper`, `lower`|
|`upsertKeyword`|Upsert keyword|You can choose different upsert keywords|String|`INSERT`|`INSERT`, `INSERT ALL`, `UPDATE OR`, `UPSERT INTO`, `REPLACE INTO`, `ON DUPLICATE KEY UPDATE`, `ON CONFLICT`|
|`insertOnConflict`|On conflict expression|Expression for the end of the statement. Enter the required value in this field.<br>This is database specific setting|String|*&lt;empty&gt;*|*Any*|

#### Source code (`source.code`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`language`|Language|Programming languages|String|`PHP &lt; 5.4`|`PHP &lt; 5.4`, `PHP 5.4+`|
|`formatDateISOPHP`|Format dates in ISO 8601|&nbsp;|Boolean|`true`|*Any*|
|`extension`|File extension|&nbsp;|String|`php`|*Any*|
|`quoteChar`|Quote character|Character which will be used to quote strings|String|`"`|`"`, `'`|
|`rowDelimiter`|Row delimiter|Row delimiter. Default is system-specific line feed delimiter.<br> You can use special characters \ + t,n,r|String|`default`|`default`, `\n`, `\r`, `\r\n`, `\n\r`|

#### TXT (`txt`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`extension`|File extension|&nbsp;|String|`txt`|*Any*|
|`batchSize`|Batch size|&nbsp;|String|`200`|*Any*|
|`minColumnLength`|Min column length|&nbsp;|String|`3`|*Any*|
|`maxColumnLength`|Max column length|&nbsp;|String|`0`|*Any*|
|`showNulls`|Show NULLs|&nbsp;|Boolean|`false`|*Any*|
|`delimHeader`|Show header delimiter|&nbsp;|Boolean|`true`|*Any*|
|`delimLeading`|Show leading delimiter|&nbsp;|Boolean|`true`|*Any*|
|`delimTrailing`|Show trailing delimiter|&nbsp;|Boolean|`true`|*Any*|
|`delimBetween`|Show in-between delimiter|&nbsp;|Boolean|`true`|*Any*|

#### XML (`xml`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`extension`|File extension|&nbsp;|String|`xml`|*Any*|

#### XLSX (`xlsx`)
|Id|Name|Description|Type|Default Value|Allowed Values|
|---|---|---|---|---|---|
|`extension`|File extension|&nbsp;|String|`xlsx`|*Any*|
|`rownumber`|Row number(s)|Set row index as first column|Boolean|`false`|*Any*|
|`border`|Border style|Cell borders style|String|`THIN`|`NONE`, `THIN`, `THICK`|
|`nullString`|NULL string|String which will be used instead of NULL values|String|*&lt;empty&gt;*|*Any*|
|`header`|Column names as header|Use column name as first row|Boolean|`true`|*Any*|
|`headerfont`|Header row font|First row font properties|String|`BOLD`|`NONE`, `BOLD`, `ITALIC`, `STRIKEOUT`, `UNDERLINE`|
|`trueString`|Boolean string TRUE|String which will be used instead of TRUE boolean values|String|`true`|*Any*|
|`falseString`|Boolean string FALSE|String which will be used instead of FALSE boolean values|String|`false`|*Any*|
|`exportSql`|Export SQL|Export SQL to a second sheet|Boolean|`false`|*Any*|
|`splitSqlText`|Split SQL Text|Split exported SQL on rows by CR|Boolean|`false`|*Any*|
|`splitByRowCount`|Max row on sheet|Split by row count|Integer|`1048575`|*Any*|
|`splitByColNum`|Column group|Column number for grouping rows on sheet by column value|Integer|`0`|*Any*|
|`dateFormat`|Excel date format|Excel date and time format (e.g. m/d/yy h:mm) it can be changed in Excel application|String|`m/d/yy`|`m/d/yy`, `d-mmm-yy`, `d-mmm`, `mmm-yy`, `h:mm AM/PM`, `h:mm:ss AM/PM`, `h:mm`, `h:mm:ss`, `m/d/yy h:mm`|
