# AdGroupSelector
Provides methods for selecting ad groups from the account.

Example usage:
```javascript
var adGroupSelector = BingAdsApp
     .adGroups()
     .withCondition("Impressions > 100")
     .forDateRange("LAST_MONTH")
     .orderBy("Clicks DESC");

 var adGroupIterator = adGroupSelector.get();
 while (adGroupIterator.hasNext()) {
   var adGroup = adGroupIterator.next();
 }
```

See also:
- [AdGroupIterator](./AdGroupIterator)
- [AdGroup](./AdGroup)

# Methods
|Method Name|Return Type|Description|
|-|-|-
[forDateRange(Object dateFrom, Object dateTo)](#fordaterange~object-datefrom_-object-dateto~)|[AdGroupSelector](./AdGroupSelector)|Returns a selector with the specified start and end dates applied.
[forDateRange(String dateRange)](#fordaterange~string-daterange~)|[AdGroupSelector](./AdGroupSelector)|Returns a selector with the predefined date range applied.
[get](#get)|[AdGroupIterator](./AdGroupIterator)|Returns the iterator that you use to get the ad groups based on the selector's selection criteria.
[orderBy(String orderBy)](#orderby~string-orderby~)|[AdGroupSelector](./AdGroupSelector)|Returns a selector with the specified ordering applied.
[withCondition(String condition)](#withcondition~string-condition~)|[AdGroupSelector](./AdGroupSelector)|Returns a selector that limits the ad groups it returns to those that match the filter criteria.
[withIds(long[] ids)](#withids~long-ids~)|[AdGroupSelector](./AdGroupSelector)|Returns a selector that returns only ad groups with the specified IDs.
[withLimit(int limit)](#withlimit~int-limit~)|[AdGroupSelector](./AdGroupSelector)|Returns a selector that limits the number of ad groups it returns to the top <i>n</i> ad groups that match the selection criteria.

## <a name="fordaterange~object-datefrom_-object-dateto~"></a>forDateRange(Object dateFrom, Object dateTo)
Returns a selector with the specified start and end dates applied.

You may specify the date parameters using strings or objects. To use strings, specify the date in the form, YYYYMMDD. If you use objects, create a JSON object with the following fields:  

- year
- month
- day

For example, {year: 2016, month: 5, day: 13}.

The date range is inclusive.

If you apply conditions or ordering that reference performance metric fields, you must specify a date range.  Only the last date range specified will be used.

### Arguments:
|Name|Type|Description|
|-|-|-
dateFrom|Object|Start date of the date range.
dateTo|Object|End date of the date range.
### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|Selector with date range applied.

## <a name="fordaterange~string-daterange~"></a>forDateRange(String dateRange)
Returns a selector with the predefined date range applied.

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

If you apply conditions or ordering that reference performance metric fields, you must specify a date range.  Only the last date range specified will be used.

### Arguments:
|Name|Type|Description|
|-|-|-
dateRange|String|Date range to apply to the selector.
### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|Selector with date range applied.

## <a name="get"></a>get
Returns the iterator that you use to get the ad groups based on the selector's selection criteria.
### Returns:
|Type|Description|
|-|-
[AdGroupIterator](./AdGroupIterator)|Iterator used to get the ad groups in this selector.

## <a name="orderby~string-orderby~"></a>orderBy(String orderBy)
Returns a selector with the specified ordering applied.

Specify the orderBy parameter in the form, "columnName orderDirection" where:

- columnName is a supported column, see [Supported Columns](#supported-ad-group-columns).
- orderDirection is the direction to order the results in. Set to ASC to order the results in ascending order or DESC to order the results in descending order. The default is ASC.


For example, the following call returns results in ascending order by MaxCpc.

<code>agSelector = agSelector.orderBy("MaxCpc");</code>


Only one orderBy column is supported.
### Arguments:
|Name|Type|Description|
|-|-|-
orderBy|String|Ordering to apply.
### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|Selector with ordering applied.

## <a name="withcondition~string-condition~"></a>withCondition(String condition)
Returns a selector that limits the ad groups it returns to those that match the filter criteria.

Specify the condition parameter in the form, "columnName operator value" where: 

- columnName is the name of a performance metric to order the results by. For a list of possible values, see [Supported Columns](#supported-ad-group-columns).  If you set columName to a performance metric column name, you must also specify a date range using [forDateRange(String dateRange)](#fordaterange~string-daterange~) or [forDateRange(Object dateFrom, Object dateTo)](#fordaterange~object-datefrom_-object-dateto~).
- operator is one of the supported [operators](#operators).

### Operators
The operator that can be used in a condition depends on the type of column. 
For Integer and Long columns: 

```
<  <=  >  >=  =  !=
```
For Double columns: 
```
<  >
```
For String columns: 
```
=  !=  STARTS_WITH  STARTS_WITH_IGNORE_CASE  CONTAINS
 CONTAINS_IGNORE_CASE  DOES_NOT_CONTAIN  DOES_NOT_CONTAIN_IGNORE_CASE
```
For Enumeration columns: 
```
=  !=  IN []  NOT_IN []
```

Operators are case-sensitive: `starts_with` won't work. 

<a name="supported-ad-group-columns"></a>
### Supported Columns
Supported columns for ad group filtering. 

|Column|Type|Example|Bing Web UI filter|
|-|-|-|-
<strong>Stats</strong>|
AverageCpc|double|`withCondition("AverageCpc < 1.45")`|Avg. CPC
AverageCpm|double|`withCondition("AverageCpm > 0.48")`|Avg. CPM
AveragePageviews|double|`withCondition("AveragePageviews > 0")`|
AveragePosition|double|`withCondition("AveragePosition > 7.5")`|Avg. pos.
BounceRate|double|`withCondition("BounceRate < 0.5")`|
ClickConversionRate|double|`withCondition("ClickConversionRate > 0.1")`|Conv. Rate
Clicks|long|`withCondition("Clicks >= 21")`|Clicks
ConvertedClicks|long|`withCondition("ConvertedClicks <= 4")`|Conv.
Cost|double|`withCondition("Cost > 4.48")`.<br /> The value is in the currency of the account.|Spend
Ctr|double|`withCondition("Ctr > 0.01")`.<br /> Note that the Ctr is in the range 0..1, so a 5% Ctr is represented as 0.05.|CTR
Impressions|long|`withCondition("Impressions != 0")`|Impr.
&nbsp;|&nbsp;|&nbsp;|&nbsp;
<strong>Ad group attributes</strong>|
Status|Enumeration:<br />&nbsp;`ENABLED`<br />&nbsp;`PAUSED`<br />&nbsp;`REMOVED`|`withCondition("Status = PAUSED")`|
Name|String|`withCondition("Name CONTAINS_IGNORE_CASE 'shoes'")`|Ad group name
CampaignName|String|`withCondition("CampaignName CONTAINS_IGNORE_CASE 'promotion'")`|Campaign name
KeywordMaxCpc|double|`withCondition("KeywordMaxCpc > 10.0")`.<br /> The value is in the currency of the account.|
CampaignStatus|Enumeration:<br />&nbsp;`ENABLED`<br />&nbsp;`PAUSED`<br />&nbsp;`REMOVED`|`withCondition("CampaignStatus = ENABLED")`.<br /> Use to return ad groups from only ENABLED campaigns.|
&nbsp;|&nbsp;|&nbsp;|&nbsp;
### Arguments:
|Name|Type|Description|
|-|-|-
condition|String|Condition to add to the selector.
### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|Selector with the condition applied.

## <a name="withids~long-ids~"></a>withIds(long[] ids)
Returns a selector that returns only ad groups with the specified IDs.


You may apply one or more conditions to a selector. A chain of conditions is considered an AND operation. If condition A is true AND condition B is true, select the entity. For example, the following call selects only ad group 33333.

```javascript
BingAdsApp.adGroups()
    .withIds([11111, 22222, 33333])
    .withIds([33333, 44444, 55555])
```

### Arguments:
|Name|Type|Description|
|-|-|-
ids|long[]|Array of ad group IDs. The maximum number of IDs that you may specify is 1,000. If you specify more than 1,000 IDs, calling the get method will fail.
### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|Selector restricted to the given IDs.

## <a name="withlimit~int-limit~"></a>withLimit(int limit)
Returns a selector that limits the number of ad groups it returns to the top <i>n</i> ad groups that match the selection criteria.
### Arguments:
|Name|Type|Description|
|-|-|-
limit|int|The number of entities to return.
### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|Selector with limit applied.

