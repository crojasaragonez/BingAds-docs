# Range
This class represents a range of cells in a worksheet.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[copyTo(Range destination)](#copyto~range-destination~)|void|Copies content and formatting information from this range to the target range.<br />
[getAddress](#getaddress)|String|Get the address of this range.<br />
[getColumn](#getcolumn)|long|Returns the starting column position for this range.<br />
[getFormula](#getformula)|String|Returns the formula (in A1 notation), if defined, for the top-left cell of this range.<br />
[getLastRow](#getlastrow)|long|Returns the position of the last row of this range.<br />
[getNumColumns](#getnumcolumns)|long|Returns the number of columns in this range.<br />
[getNumRows](#getnumrows)|long|Returns the number of rows in this range.<br />
[getRow](#getrow)|long|Returns the position of the row for this range.<br />
[getValue](#getvalue)|Object|Returns the value contained by the top-left cell in this range.<br />
[getValues](#getvalues)|Object[][]|Returns a two-dimensional array of values contained by this range, beginning with the top-left cell.<br />
[isBlank](#isblank)|boolean|Returns <br />
[setFontSize(long size)](#setfontsize~long-size~)|[Range](./Range)|Sets the specified point size to use for fonts on all the cells in this range.<br />
[setFontWeight(String fontWeight)](#setfontweight~string-fontweight~)|[Range](./Range)|Sets the specified point weight to use for fonts on all the cells in this range. Valid values include 'normal' and 'bold'.<br />
[setHorizontalAlignment(String alignment)](#sethorizontalalignment~string-alignment~)|[Range](./Range)|Sets the horizontal alignment of content in the cells in this range. Valid values include 'left', 'center' or 'normal'.<br />
[setValue(Object value)](#setvalue~object-value~)|[Range](./Range)|Sets the value to all cells in this range.<br />
[setValues(Object[][] values)](#setvalues~object[]-values~)|[Range](./Range)|Sets the specified values to the cells in this range, assigning each value to the cell based on matching row and column positions. The dimensions of the input value array must match the dimensions of this range.<br />
[setVerticalAlignment(String alignment)](#setverticalalignment~string-alignment~)|[Range](./Range)|Sets the vertical alignment of content in the cells in this range. Valid values include 'top', 'middle' or 'bottom'.<br />
&nbsp;|&nbsp;|&nbsp;

## <a name="copyto~range-destination~"></a>copyTo(Range destination)
Copies content and formatting information from this range to the target range.

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="getaddress"></a>getAddress
Get the address of this range.




### Returns:
|Type|Description|
|-|-
String|The address of the range.
&nbsp;|&nbsp;
## <a name="getcolumn"></a>getColumn
Returns the starting column position for this range.

### Returns:
|Type|Description|
|-|-
long|
&nbsp;|&nbsp;
## <a name="getformula"></a>getFormula
Returns the formula (in A1 notation), if defined, for the top-left cell of this range.

### Returns:
|Type|Description|
|-|-
String|
&nbsp;|&nbsp;
## <a name="getlastrow"></a>getLastRow
Returns the position of the last row of this range.

### Returns:
|Type|Description|
|-|-
long|
&nbsp;|&nbsp;
## <a name="getnumcolumns"></a>getNumColumns
Returns the number of columns in this range.

### Returns:
|Type|Description|
|-|-
long|
&nbsp;|&nbsp;
## <a name="getnumrows"></a>getNumRows
Returns the number of rows in this range.

### Returns:
|Type|Description|
|-|-
long|
&nbsp;|&nbsp;
## <a name="getrow"></a>getRow
Returns the position of the row for this range.

### Returns:
|Type|Description|
|-|-
long|
&nbsp;|&nbsp;
## <a name="getvalue"></a>getValue
Returns the value contained by the top-left cell in this range.

### Returns:
|Type|Description|
|-|-
Object|
&nbsp;|&nbsp;
## <a name="getvalues"></a>getValues
Returns a two-dimensional array of values contained by this range, beginning with the top-left cell.

### Returns:
|Type|Description|
|-|-
Object[][]|
&nbsp;|&nbsp;
## <a name="isblank"></a>isBlank
Returns 

### Returns:
|Type|Description|
|-|-
boolean|
&nbsp;|&nbsp;
## <a name="setfontsize~long-size~"></a>setFontSize(long size)
Sets the specified point size to use for fonts on all the cells in this range.

### Returns:
|Type|Description|
|-|-
[Range](./Range)|
&nbsp;|&nbsp;
## <a name="setfontweight~string-fontweight~"></a>setFontWeight(String fontWeight)
Sets the specified point weight to use for fonts on all the cells in this range. Valid values include 'normal' and 'bold'.

### Arguments:
|Name|Type|Description|
|-|-|-
fontWeight|String|The font weight, either 'bold' or 'normal'.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Range](./Range)|
&nbsp;|&nbsp;
## <a name="sethorizontalalignment~string-alignment~"></a>setHorizontalAlignment(String alignment)
Sets the horizontal alignment of content in the cells in this range. Valid values include 'left', 'center' or 'normal'.

### Arguments:
|Name|Type|Description|
|-|-|-
alignment|String|The alignment to use.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Range](./Range)|
&nbsp;|&nbsp;
## <a name="setvalue~object-value~"></a>setValue(Object value)
Sets the value to all cells in this range.

### Arguments:
|Name|Type|Description|
|-|-|-
value|Object|the value for the range
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Range](./Range)|
&nbsp;|&nbsp;
## <a name="setvalues~object[]-values~"></a>setValues(Object[][] values)
Sets the specified values to the cells in this range, assigning each value to the cell based on matching row and column positions. The dimensions of the input value array must match the dimensions of this range.

### Arguments:
|Name|Type|Description|
|-|-|-
values|Object[][]|a two-dimensional array of values
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Range](./Range)|
&nbsp;|&nbsp;
## <a name="setverticalalignment~string-alignment~"></a>setVerticalAlignment(String alignment)
Sets the vertical alignment of content in the cells in this range. Valid values include 'top', 'middle' or 'bottom'.

### Arguments:
|Name|Type|Description|
|-|-|-
alignment|String|The alignment to use.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Range](./Range)|
&nbsp;|&nbsp;
