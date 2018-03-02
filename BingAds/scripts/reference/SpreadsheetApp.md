# SpreadsheetApp
This class allows users to open and create spreadsheets on OneDrive.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[create(String name)](#create~string-name~)|[Spreadsheet](./Spreadsheet)|Creates a new spreadsheet with the specified name.<br />
[openById(String id)](#openbyid~string-id~)|[Spreadsheet](./Spreadsheet)|Opens the spreadsheet with the specified ID.<br />
[openByName(String name)](#openbyname~string-name~)|[Spreadsheet](./Spreadsheet)|Opens the spreadsheet identified by the specified name.<br />

## <a name="create~string-name~"></a>create(String name)
Creates a new spreadsheet with the specified name.

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The name for the new spreadsheet.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Spreadsheet](./Spreadsheet)|A new spreadsheet.
&nbsp;|&nbsp;
## <a name="openbyid~string-id~"></a>openById(String id)
Opens the spreadsheet with the specified ID.

### Returns:
|Type|Description|
|-|-
[Spreadsheet](./Spreadsheet)|The spreadsheet with the specified ID.
&nbsp;|&nbsp;
## <a name="openbyname~string-name~"></a>openByName(String name)
Opens the spreadsheet identified by the specified name.

### Arguments:
|Name|Type|Description|
|-|-|-
arg1|String|The name of the spreadsheet to open.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[Spreadsheet](./Spreadsheet)|The spreadsheet identified by the specified name.
&nbsp;|&nbsp;
