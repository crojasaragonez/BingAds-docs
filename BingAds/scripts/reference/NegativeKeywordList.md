# NegativeKeywordList
Represents a keyword.
# Methods
|Method Name|Return Type|Description|
|-|-|-
[addNegativeKeyword(String keywordText)](#addnegativekeyword~string-keywordtext~)|void|Adds a keyword to the negative keyword list.
[addNegativeKeywords(String keywordText)](#addnegativekeywords~string-keywordtext~)|void|Adds a list of keywords to the negative keyword list.
[getEntityType](#getentitytype)|String|Returns the entity type of this negative keyword list, which is "NegativeKeywordList".<br />
[getId](#getid)|long|Returns the ID of this negative keyword list.<br />
[getName](#getname)|String|Returns the name of this negative keyword list.<br />
[setName(String name)](#setname~string-name~)|void|Sets the name of this negative keyword list.<br />

## <a name="addnegativekeyword~string-keywordtext~"></a>addNegativeKeyword(String keywordText)
Adds a keyword to the negative keyword list.

To specify match type for the new negative keyword:

- negativeKeywordList.addNegativeKeyword("shoes") - broad match.
- negativeKeywordList.addNegativeKeyword("\"shoes\"") - phrase match.
- negativeKeywordList.addNegativeKeyword("[leather shoes]") - exact match.

### Arguments:
|Name|Type|Description|
|-|-|-
keywordText|String|The text of the negative keyword.<br />
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="addnegativekeywords~string-keywordtext~"></a>addNegativeKeywords(String keywordText)
Adds a list of keywords to the negative keyword list.

To specify match type for the new negative keyword:

- negativeKeywordsList.addNegativeKeywords(["planes", "trains"]) - broad match.
- negativeKeywordsList.addNegativeKeywords(["\"planes\"", "\"trains\""]) - phrase match.
- negativeKeywordsList.addNegativeKeywords(["[model planes]", "[toy trains]") - exact match.
### Arguments:
|Name|Type|Description|
|-|-|-
keywordTexts|String[]|An array of keyword strings.<br />
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="getentitytype"></a>getEntityType
Returns the entity type of this negative keyword list, which is "NegativeKeywordList".



### Returns:
|Type|Description|
|-|-
String|The entity type of this negative keyword list, which is "NegativeKeywordList".

## <a name="getid"></a>getId
Returns the ID of this negative keyword list.

### Returns:
|Type|Description|
|-|-
long|The ID of this negative keyword list.

## <a name="getname"></a>getName
Returns the name of this negative keyword list.

### Returns:
|Type|Description|
|-|-
String|The name of this negative keyword list.

## <a name="setname~string-name~"></a>setName(String name)
Sets the name of this negative keyword list.


### Arguments:
|Name|Type|Description|
|-|-|-
name|String|the new name for this negative keyword list.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

