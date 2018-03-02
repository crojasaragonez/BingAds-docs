# Keyword
Represents a keyword.
Example usage:
```javascript
 var stats = keyword.getStatsFor("THIS_MONTH");
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[bidding](#bidding)|[KeywordBidding](./KeywordBidding)|Provides methods to access information about the keywords bidding.<br />
[clearDestinationUrl](#cleardestinationurl)|void|Clears the destination URL of this keyword. <br />
[enable](#enable)|void|Enables this keyword.<br />
[getAdGroup](#getadgroup)|[AdGroup](AdGroup)|Returns the parent ad group of this keyword.<br />
[getCampaign](#getcampaign)|[Campaign](./Campaign)|Returns the parent campaign of this keyword.<br />
[getEntityType](#getentitytype)|String|Returns the entity type of this keyword, which is "Keyword".<br />
[getId](#getid)|long|Returns the ID of this keyword.<br />
[getMatchType](#getmatchtype)|String|Returns the match type of this keyword.<br />
[getStats](#getstats)|[Stats](./Stats)|Returns statistics for the keyword.<br />
[getText](#gettext)|String|Returns the text of this keyword.<br />
[isEnabled](#isenabled)|boolean|Returns true if this keyword is enabled <br />
[isPaused](#ispaused)|boolean|Returns true if this keyword is paused. <br />
[pause](#pause)|void|Pauses this keyword.<br />
[remove](#remove)|void|Removes this keyword.<br />
[urls](#urls)|[KeywordUrls](./KeywordUrls)|Returns the URL fields of this keyword.<br />

## <a name="bidding"></a>bidding
Provides methods to access information about the keywords bidding.




### Returns:
|Type|Description|
|-|-
[KeywordBidding](./KeywordBidding)|Methods to access information about the keywords bidding.
&nbsp;|&nbsp;
## <a name="cleardestinationurl"></a>clearDestinationUrl
Clears the destination URL of this keyword. 

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="enable"></a>enable
Enables this keyword.

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="getadgroup"></a>getAdGroup
Returns the parent ad group of this keyword.

### Returns:
|Type|Description|
|-|-
[AdGroup](AdGroup)|The parent ad group of this keyword.
&nbsp;|&nbsp;
## <a name="getcampaign"></a>getCampaign
Returns the parent campaign of this keyword.

### Returns:
|Type|Description|
|-|-
[Campaign](./Campaign)|The parent campaign of this keyword.
&nbsp;|&nbsp;
## <a name="getentitytype"></a>getEntityType
Returns the entity type of this keyword, which is "Keyword".

### Returns:
|Type|Description|
|-|-
String|The entity type of this keyword, which is "Keyword".
&nbsp;|&nbsp;
## <a name="getid"></a>getId
Returns the ID of this keyword.

### Returns:
|Type|Description|
|-|-
long|The ID of this keyword.
&nbsp;|&nbsp;
## <a name="getmatchtype"></a>getMatchType
Returns the match type of this keyword.


Possible return values are:

- BROAD
- PHRASE
- EXACT


### Returns:
|Type|Description|
|-|-
String|The match type of this keyword.
&nbsp;|&nbsp;
## <a name="getstats"></a>getStats
Returns statistics for the keyword.




### Returns:
|Type|Description|
|-|-
[Stats](./Stats)|The statistics for the keyword.
&nbsp;|&nbsp;
## <a name="gettext"></a>getText
Returns the text of this keyword.


The text will be returned in one of the following formats based on the match type:

- `books` - broad match
- `"books"` - phrase match
- `[hardcover books]` - exact match


### Returns:
|Type|Description|
|-|-
String|The text of this keyword.
&nbsp;|&nbsp;
## <a name="isenabled"></a>isEnabled
Returns true if this keyword is enabled 

### Returns:
|Type|Description|
|-|-
boolean|True if this keyword is enabled.
&nbsp;|&nbsp;
## <a name="ispaused"></a>isPaused
Returns true if this keyword is paused. 

### Returns:
|Type|Description|
|-|-
boolean|True if the keyword is paused.
&nbsp;|&nbsp;
## <a name="pause"></a>pause
Pauses this keyword.

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="remove"></a>remove
Removes this keyword.

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="urls"></a>urls
Returns the URL fields of this keyword.

### Returns:
|Type|Description|
|-|-
[KeywordUrls](./KeywordUrls)|The URL fields of this keyword.
&nbsp;|&nbsp;
