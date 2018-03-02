# Spreadsheet
This class represents a spreadsheet.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[getId](#getid)|String|Returns the unique ID for this spreadsheet.<br />
[getName](#getname)|String|Returns the name of this spreadsheet.<br />
[getSheetByName(String name)](#getsheetbyname~string-name~)|[Sheet](./Sheet)|Returns the sheet with the specified name.
[getSheets](#getsheets)|[Sheet[]](./Sheet)|Returns all the sheets in this spreadsheet.<br />
[insertSheet](#insertsheet)|[Sheet](./Sheet)|Inserts a new sheet in this spreadsheet using the default name and makes it the active sheet.<br />
&nbsp;|&nbsp;|&nbsp;

## <a name="getid"></a>getId
Returns the unique ID for this spreadsheet.

### Returns:
|Type|Description|
|-|-
String|The unique ID for this spreadsheet.
&nbsp;|&nbsp;
## <a name="getname"></a>getName
Returns the name of this spreadsheet.

### Returns:
|Type|Description|
|-|-
String|The name of this spreadsheet.
&nbsp;|&nbsp;
## <a name="getsheetbyname~string-name~"></a>getSheetByName(String name)
Returns the sheet with the specified name.
### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The name of the sheet to get.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The sheet with the specified name.
&nbsp;|&nbsp;
## <a name="getsheets"></a>getSheets
Returns all the sheets in this spreadsheet.

### Returns:
|Type|Description|
|-|-
[Sheet[]](./Sheet)|An array of all the sheets in this spreadsheet.
&nbsp;|&nbsp;
## <a name="insertsheet"></a>insertSheet
Inserts a new sheet in this spreadsheet using the default name and makes it the active sheet.

### Returns:
|Type|Description|
|-|-
[Sheet](./Sheet)|The new sheet.
&nbsp;|&nbsp;