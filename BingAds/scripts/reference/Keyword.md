# Keyword
Represents a keyword.
See also:

- [KeywordSelector](./KeywordSelector)
- [KeywordIterator](./KeywordIterator)


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
[getStatsFor(String dateRange)](#getstatsfor~string-daterange~)|[Stats](./Stats)|Returns an object which provides statistics for the specified predefined date range.

## <a name="bidding"></a>bidding
Provides methods to access information about the keywords bidding.



### Returns:
|Type|Description|
|-|-
[KeywordBidding](./KeywordBidding)|Methods to access information about the keywords bidding.

## <a name="cleardestinationurl"></a>clearDestinationUrl
Clears the destination URL of this keyword. 

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="enable"></a>enable
Enables this keyword.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="getadgroup"></a>getAdGroup
Returns the parent ad group of this keyword.

### Returns:
|Type|Description|
|-|-
[AdGroup](AdGroup)|Parent ad group of this keyword.

## <a name="getcampaign"></a>getCampaign
Returns the parent campaign of this keyword.

### Returns:
|Type|Description|
|-|-
[Campaign](./Campaign)|Parent campaign of this keyword.

## <a name="getentitytype"></a>getEntityType
Returns the entity type of this keyword, which is "Keyword".

### Returns:
|Type|Description|
|-|-
String|Entity type of this keyword, which is "Keyword".

## <a name="getid"></a>getId
Returns the ID of this keyword.

### Returns:
|Type|Description|
|-|-
long|ID of this keyword.

## <a name="getmatchtype"></a>getMatchType
Returns the match type of this keyword.


Possible return values are:

- BROAD
- PHRASE
- EXACT

### Returns:
|Type|Description|
|-|-
String|Match type of this keyword.

## <a name="getstats"></a>getStats
Returns statistics for the keyword.



### Returns:
|Type|Description|
|-|-
[Stats](./Stats)|Statistics for the keyword.

## <a name="gettext"></a>getText
Returns the text of this keyword.


The text will be returned in one of the following formats based on the match type:

- `books` - broad match
- `"books"` - phrase match
- `[hardcover books]` - exact match

### Returns:
|Type|Description|
|-|-
String|Text of this keyword.

## <a name="isenabled"></a>isEnabled
Returns true if this keyword is enabled 

### Returns:
|Type|Description|
|-|-
boolean|Boolean value that determines if this keyword is enabled.

## <a name="ispaused"></a>isPaused
Returns true if this keyword is paused. 

### Returns:
|Type|Description|
|-|-
boolean|Boolean value that determines if the keyword is paused.

## <a name="pause"></a>pause
Pauses this keyword.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="remove"></a>remove
Removes this keyword.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="urls"></a>urls
Returns the URL fields of this keyword.

### Returns:
|Type|Description|
|-|-
[KeywordUrls](./KeywordUrls)|URL fields of this keyword.

## <a name="getstatsfor~string-daterange~"></a>getStatsFor(String dateRange)
Returns an object which provides statistics for the specified predefined date range.

Supported date range values:



- TODAY
- YESTERDAY

- LAST_7_DAYS

- THIS_WEEK_SUN_TODAY

- LAST_14_DAYS
- LAST_30_DAYS

- LAST_WEEK_SUN_SAT

- THIS_MONTH
- LAST_MONTH
- ALL_TIME



Example:

```

keyword.getStatsFor("THIS_MONTH");
```



Date range must be specified if the selector has conditions or ordering for metrics statistics applied.  Only the last date range specified will be used.

### Arguments:
|Name|Type|Description|
|-|-|-
dateRange|String|Date range for which the stats are requested.
### Returns:
|Type|Description|
|-|-
[Stats](./Stats)|Stats for the specified date range.

