# ExpandedTextAd
Represents an expanded text ad in Bing Ads.

Example usage:
```javascript
 var stats = ad.getStatsFor("THIS_MONTH");
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[asType](#astype)|[AdViewSpace](./AdViewSpace)|Returns properties specific to the type of this ad.
[enable](#enable)|void|Enables the ad.<br />
[getAdGroup](#getadgroup)|[AdGroup](./AdGroup)|Returns the parent ad group of this ad.<br />
[getApprovalStatus](#getapprovalstatus)|String|Returns the approval status of the ExpandedTextAD.
[getCampaign](#getcampaign)|[Campaign](./Campaign)|Returns the parent campaign of this ad.<br />
[getDescription](#getdescription)|String|Returns the description of this ad.<br />
[getDisapprovalReasons](#getdisapprovalreasons)|String[]|Returns an array containing the reasons for which this ad was disapproved. If it is not disapproved, the array will be empty.<br />
[getEntityType](#getentitytype)|String|Returns the type of entity of this ad, which is “Ad”.<br />
[getHeadlinePart1](#getheadlinepart1)|String|Returns the first part of the headline (title) of this ad. <br />
[getHeadlinePart2](#getheadlinepart2)|String|Returns the second part of the headline (title) of this ad. <br />
[getId](#getid)|long|Returns the ID of this ad. In order to specify a unique ID for an ad, both its ad group ID and this ID need to be specified. <br />
[getPath1](#getpath1)|String|Returns the first path that appears with this ad's display URL.<br />
[getPath2](#getpath2)|String|Returns the second path that appears with this ad's display URL.<br />
[getStatsFor(Object dateFrom, Object dateTo)](#getstatsfor~object-datefrom_-object-dateto~)|[Stats](./Stats)|Returns a [Stats](./Stats) object for this expanded text ad for the specified date range.
[getStatsFor(String dateRange)](#getstatsfor~string-daterange~)|[Stats](./Stats)|Returns an object which provides statistics for the specified predefined date range.
[getType](#gettype)|String|Returns the type of this ad.<br />
[isEnabled](#isenabled)|boolean|Returns true if this ad is enabled. <br />
[isPaused](#ispaused)|boolean|Returns true if this ad is paused <br />
[isType](#istype)|[AdTypeSpace](./AdTypeSpace)|Returns an object which provides more information about the type of this ad.
[pause](#pause)|void|Pauses this ad.<br />
[remove](#remove)|void|Removes this ad.<br />
[urls](#urls)|[AdUrls](./AdUrls)|Returns an AdUrls object which provides access to the URL fields of this <br />

## <a name="astype"></a>asType
Returns properties specific to the type of this ad.
### Returns:
|Type|Description|
|-|-
[AdViewSpace](./AdViewSpace)|A starting point for viewing type-specific ad information.

## <a name="enable"></a>enable
Enables the ad.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="getadgroup"></a>getAdGroup
Returns the parent ad group of this ad.

### Returns:
|Type|Description|
|-|-
[AdGroup](./AdGroup)|The ad group to which this ad belongs.

## <a name="getapprovalstatus"></a>getApprovalStatus
Returns the approval status of the ExpandedTextAD.

Possible values:

- APPROVED
- DISAPPROVED
### Returns:
|Type|Description|
|-|-
String|

## <a name="getcampaign"></a>getCampaign
Returns the parent campaign of this ad.

### Returns:
|Type|Description|
|-|-
[Campaign](./Campaign)|The campaign to which this ad belongs.

## <a name="getdescription"></a>getDescription
Returns the description of this ad.

### Returns:
|Type|Description|
|-|-
String|The description of the ad.

## <a name="getdisapprovalreasons"></a>getDisapprovalReasons
Returns an array containing the reasons for which this ad was disapproved. If it is not disapproved, the array will be empty.

### Returns:
|Type|Description|
|-|-
String[]|

## <a name="getentitytype"></a>getEntityType
Returns the type of entity of this ad, which is “Ad”.

### Returns:
|Type|Description|
|-|-
String|Type of this entity: "Ad".

## <a name="getheadlinepart1"></a>getHeadlinePart1
Returns the first part of the headline (title) of this ad. 

### Returns:
|Type|Description|
|-|-
String|The first part of the ad's headline.

## <a name="getheadlinepart2"></a>getHeadlinePart2
Returns the second part of the headline (title) of this ad. 

### Returns:
|Type|Description|
|-|-
String|The second part of the ad's headline.

## <a name="getid"></a>getId
Returns the ID of this ad. In order to specify a unique ID for an ad, both its ad group ID and this ID need to be specified. 

### Returns:
|Type|Description|
|-|-
long|The ID of the ad.

## <a name="getpath1"></a>getPath1
Returns the first path that appears with this ad's display URL.

### Returns:
|Type|Description|
|-|-
String|The first path that appears with the ad's displayed URL.

## <a name="getpath2"></a>getPath2
Returns the second path that appears with this ad's display URL.

### Returns:
|Type|Description|
|-|-
String|The second path that appears with the ad's displayed URL.

## <a name="getstatsfor~object-datefrom_-object-dateto~"></a>getStatsFor(Object dateFrom, Object dateTo)
Returns a [Stats](./Stats) object for this expanded text ad for the specified date range.

You may specify the date parameters using strings or objects. To use strings, specify the date in the form, YYYYMMDD. If you use objects, create a JSON object with the following fields:  

- year
- month
- day

For example, {year: 2016, month: 5, day: 13}.

The date range is inclusive on both ends.

Date range must be specified if the selector has conditions or ordering for metrics statistics applied.  Only the last date range specified will be used.

### Arguments:
|Name|Type|Description|
|-|-|-
dateFrom|Object|Start date of the date range.
dateTo|Object|End date of the date range.
### Returns:
|Type|Description|
|-|-
[Stats](./Stats)|The stats for the specified date range.

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
selector.forDateRange("LAST_7_DAYS");
```

Date range must be specified if the selector has conditions or ordering for metrics statistics applied.  Only the last date range specified will be used.

### Arguments:
|Name|Type|Description|
|-|-|-
dateRange|String|Date range for which the stats are requested.
### Returns:
|Type|Description|
|-|-
[Stats](./Stats)|The stats for the specified date range.

## <a name="gettype"></a>getType
Returns the type of this ad.


Possible values are:

- EXPANDED_TEXT_AD
- TEXT_AD

### Returns:
|Type|Description|
|-|-
String|The type of the ad.

## <a name="isenabled"></a>isEnabled
Returns true if this ad is enabled. 

### Returns:
|Type|Description|
|-|-
boolean|A boolean value that determines if the ad is enabled.

## <a name="ispaused"></a>isPaused
Returns true if this ad is paused 

### Returns:
|Type|Description|
|-|-
boolean|A boolean value that determines if the ad is paused.

## <a name="istype"></a>isType
Returns an object which provides more information about the type of this ad.
### Returns:
|Type|Description|
|-|-
[AdTypeSpace](./AdTypeSpace)|An object that provides more information about the type of this ad.

## <a name="pause"></a>pause
Pauses this ad.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="remove"></a>remove
Removes this ad.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="urls"></a>urls
Returns an AdUrls object which provides access to the URL fields of this 

### Returns:
|Type|Description|
|-|-
[AdUrls](./AdUrls)|Access to this ad's URL fields.
