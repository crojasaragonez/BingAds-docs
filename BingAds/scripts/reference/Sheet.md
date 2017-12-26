# Sheet
This class represents a worksheet within a spreadsheet.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[deleteColumns(long columnPosition, long numColumns)](#deletecolumns~long-columnposition_-long-numcolumns~)|void|Deletes the specified number of columns starting at the specified column position.<br />
[deleteRows(long rowPosition, long numRows)](#deleterows~long-rowposition_-long-numrows~)|void|Deletes the specified number of rows in this sheet starting from the provided row index.<br />
[getColumnWidth(long columnPosition)](#getcolumnwidth~long-columnposition~)|long|Returns the width of the specified column in pixels.<br />
[getName](#getname)|String|Returns the name of the sheet.<br />
[getRange(String a1Notation)](#getrange~string-a1notation~)|[Range](./Range)|Returns a range from this sheet specified in A1 or R1C1 notation.
[getRowHeight(long rowPosition)](#getrowheight~long-rowposition~)|int|Gets the height of the specified row in pixels.<br />
[insertColumn(long columnIndex)](#insertcolumn~long-columnindex~)|[Sheet](./Sheet)|Insert a column at the specified column index.<br />
[insertColumnsAfter(long columnIndex, long numColumns)](#insertcolumnsafter~long-columnindex_-long-numcolumns~)|[Sheet](./Sheet)|Inserts the specified number of new columns after the specified column index.
[insertRow(long rowIndex)](#insertrow~long-rowindex~)|long|Insert a row at the specified index.<br />
[insertRowsAfter(long rowIndex, long numRows)](#insertrowsafter~long-rowindex_-long-numrows~)|[Sheet](./Sheet)|Inserts the specified number of new rows after the specified row index.
[setColumnWidth(long columnPosition, long width)](#setcolumnwidth~long-columnposition_-long-width~)|[Sheet](./Sheet)|Sets the width in pixels of the column at the specified position.
[setName(String name)](#setname~string-name~)|[Sheet](./Sheet)|Sets the name of this sheet.<br />
[setRowHeight(long rowPosition, long height)](#setrowheight~long-rowposition_-long-height~)|[Sheet](./Sheet)|Sets the height in pixels of the row at the specified position.
&nbsp;|&nbsp;|&nbsp;

## <a name="deletecolumns~long-columnposition_-long-numcolumns~"></a>deleteColumns(long columnPosition, long numColumns)
Deletes the specified number of columns starting at the specified column position.




### Arguments:
|Name|Type|Description|
|-|-|-
columnPosition|long|The position of the first column to delete.<br />
numColumns|long|The number of columns to delete.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="deleterows~long-rowposition_-long-numrows~"></a>deleteRows(long rowPosition, long numRows)
Deletes the specified number of rows in this sheet starting from the provided row index.

### Arguments:
|Name|Type|Description|
|-|-|-
rowPosition|long|The position of the first row to delete.<br />
numRows|long|The number of rows to delete.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="getcolumnwidth~long-columnposition~"></a>getColumnWidth(long columnPosition)
Returns the width of the specified column in pixels.

### Arguments:
|Name|Type|Description|
|-|-|-
columnPosition|long|The position of the column to examine.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
long|
&nbsp;|&nbsp;
## <a name="getname"></a>getName
Returns the name of the sheet.




### Returns:
|Type|Description|
|-|-
String|The name of the sheet.
&nbsp;|&nbsp;
## <a name="getrange~string-a1notation~"></a>getRange(String a1Notation)
Returns a range from this sheet specified in A1 or R1C1 notation.

```javascript
 // Get a range A1:D4 on sheet titled "Invoices"
 var ss = SpreadsheetApp.getActiveSpreadsheet();
 var range = ss.getRange("Invoices!A1:D4");

 // Get cell A1 on the first sheet
 var sheet = ss.getSheets()[0];
 var cell = sheet.getRange("A1");
```

### Arguments:
|Name|Type|Description|
|-|-|-
a1Notation|[Range](./Range)|Returns the range as specified in A1 notation.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Range](./Range)|The specified range.
&nbsp;|&nbsp;
## <a name="getrowheight~long-rowposition~"></a>getRowHeight(long rowPosition)
Gets the height of the specified row in pixels.




### Arguments:
|Name|Type|Description|
|-|-|-
rowPosition|int|The position of the row to examine.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
int|The row height in pixels.
&nbsp;|&nbsp;
## <a name="insertcolumn~long-columnindex~"></a>insertColumn(long columnIndex)
Insert a column at the specified column index.




### Arguments:
|Name|Type|Description|
|-|-|-
columnIndex|long|The position where the new column should be added.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The sheet, enables method chaining.
&nbsp;|&nbsp;
## <a name="insertcolumnsafter~long-columnindex_-long-numcolumns~"></a>insertColumnsAfter(long columnIndex, long numColumns)
Inserts the specified number of new columns after the specified column index.
### Arguments:
|Name|Type|Description|
|-|-|-
numColumns|long|The number of columns to add.
columnIndex|long|The position of the column after which the new columns should be added.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The sheet, enables method chaining.
&nbsp;|&nbsp;
## <a name="insertrow~long-rowindex~"></a>insertRow(long rowIndex)
Insert a row at the specified index.




### Arguments:
|Name|Type|Description|
|-|-|-
rowIndex|long|The position where the row should be inserted.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
long|The sheet, enables method chaining.
&nbsp;|&nbsp;
## <a name="insertrowsafter~long-rowindex_-long-numrows~"></a>insertRowsAfter(long rowIndex, long numRows)
Inserts the specified number of new rows after the specified row index.
### Arguments:
|Name|Type|Description|
|-|-|-
rowIndex|long|The index of the row after which the new rows should be added.<br />
numRows|long|The number of rows to insert.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The sheet, enables chaining.
&nbsp;|&nbsp;
## <a name="setcolumnwidth~long-columnposition_-long-width~"></a>setColumnWidth(long columnPosition, long width)
Sets the width in pixels of the column at the specified position.
### Arguments:
|Name|Type|Description|
|-|-|-
width|long|The width in pixels to set the column width to.<br />
columnPosition|long|The position of the column to set the width of.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The sheet, enables method chaining.
&nbsp;|&nbsp;
## <a name="setname~string-name~"></a>setName(String name)
Sets the name of this sheet.

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The new name for the sheet.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The sheet, enables method chaining.
&nbsp;|&nbsp;
## <a name="setrowheight~long-rowposition_-long-height~"></a>setRowHeight(long rowPosition, long height)
Sets the height in pixels of the row at the specified position.
### Arguments:
|Name|Type|Description|
|-|-|-
rowPosition|long|The row position to set the height of.<br />
height|long|The height in pixels to set the row height to.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The sheet, enables method chaining.
&nbsp;|&nbsp;
