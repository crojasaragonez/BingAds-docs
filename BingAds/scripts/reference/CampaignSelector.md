# CampaignSelector
Provides methods to select campaigns by using filtering and sorting.

Example usage:
```javascript
 var campaignSelector = BingAdsApp
     .campaigns()
     .withCondition("Impressions > 100")
     .forDateRange("LAST_MONTH")
     .orderBy("Clicks DESC");

 var campaignIterator = campaignSelector.get();
 while (campaignIterator.hasNext()) {
   var campaign = campaignIterator.next();
 }
```

See also:
- [CampaignIterator](./CampaignIterator)
- [Campaign](./Campaign)


# Methods
|Method Name|Return Type|Description|
|-|-|-
[forDateRange(Object dateFrom, Object dateTo)](#fordaterange~object-datefrom_-object-dateto~)|[CampaignSelector](CampaignSelector)|Returns a selector with the specified start and end dates.
[forDateRange(String dateRange)](#fordaterange~string-daterange~)|[CampaignSelector](./CampaignSelector)|Returns a selector using the specified predefined date range.
[get](#get)|[CampaignIterator](./CampaignIterator)|Returns an iterator indexing the campaigns in this selector.<br />
[orderBy(String orderBy)](#orderby~string-orderby~)|[CampaignSelector](./CampaignSelector)|Returns a selector with the specified ordering.
[withCondition(String condition)](#withcondition~string-condition~)|[CampaignSelector](./CampaignSelector)|Returns a selector with the specified filtering conditions.
[withIds(long[] ids)](#withids~long-ids~)|[CampaignSelector](./CampaignSelector)|Returns a selector that will return only campaigns with the specified IDs.

## <a name="fordaterange~object-datefrom_-object-dateto~"></a>forDateRange(Object dateFrom, Object dateTo)
Returns a selector with the specified start and end dates.

[!INCLUDE[date-range-objects](../includes/date-range-objects.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
dateFrom|Object|Start date of the date range.
dateTo|Object|End date of the date range.
### Returns:
|Type|Description|
|-|-
[CampaignSelector](CampaignSelector)|Selector with date range applied.

## <a name="fordaterange~string-daterange~"></a>forDateRange(String dateRange)
Returns a selector using the specified predefined date range.

[!INCLUDE[date-range-constants](../includes/date-range-constants.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
dateRange|String|Date range to set onto the selector.
### Returns:
|Type|Description|
|-|-
[CampaignSelector](./CampaignSelector)|Selector with date range applied.

## <a name="get"></a>get
Returns an iterator indexing the campaigns in this selector.

### Returns:
|Type|Description|
|-|-
[CampaignIterator](./CampaignIterator)|Iterator of the requested campaigns.

## <a name="orderby~string-orderby~"></a>orderBy(String orderBy)
Returns a selector with the specified ordering.

Specify the orderBy parameter in the form, "columnName orderDirection" where:

- columnName can only be one column which is supported by the withCondition method.
- orderDirection is the direction to order the results in. Set to ASC to order the results in ascending order or DESC to order the results in descending order. The default is ASC.

You may order the results by one or more metrics by chaining together multiple orderBy calls. For example, the following call returns results in ascending order by MaxCpc.

<code>agSelector = agSelector.orderBy("MaxCpc");</code>

### Arguments:
|Name|Type|Description|
|-|-|-
orderBy|String|Ordering to apply.
### Returns:
|Type|Description|
|-|-
[CampaignSelector](./CampaignSelector)|Selector with ordering applied.

## <a name="withcondition~string-condition~"></a>withCondition(String condition)
Returns a selector with the specified filtering conditions.

Specify the condition parameter in the form, "columnName operator value" where: 

- columnName is the name of a performance metric to order the results by. For a list of possible values, see [Supported Columns](#supported-campaign-columns).  If you set columName to a performance metric column name, you must also specify a date range using [forDateRange(String dateRange)](#fordaterange~string-daterange~) or [forDateRange(Object dateFrom, Object dateTo)](#fordaterange~object-datefrom_-object-dateto~).
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

<a name="supported-campaign-columns"></a>
Supported columns for campaign filtering. 

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
Cost|double|`withCondition("Cost > 4.48")`. The value is in the currency of the account.|Spend
Ctr|double|`withCondition("Ctr > 0.01")`. Ctr is returned in 0..1 range, so 5% Ctr is represented as 0.05.|CTR
Impressions|long|`withCondition("Impressions != 0")`|Impr.
&nbsp;|&nbsp;|&nbsp;|&nbsp;
<strong>Campaign attributes</strong>|
Status|Enumeration:<br />&nbsp;ENABLED<br />&nbsp;PAUSED<br />&nbsp;REMOVED<br />&nbsp;BUDGET_PAUSED<br />&nbsp;BUDGET_AND_USER_PAUSED|`withCondition("Status = PAUSED")`|Campaign status
Name|String|`withCondition("Name CONTAINS_IGNORE_CASE 'promotion'")`|Campaign name
Budget|double|`withCondition("Budget > 10.0")`|Budget
Type|Enumeration:<br />&nbsp;SEARCH_AND_CONTENT<br />&nbsp;SHOPPING<br />&nbsp;DYNAMIC_SEARCH_ADS|`withCondition("Type = 'SEARCH_AND_CONTENT'")`|Bing-specific filter
BudgetType|Enumeration:<br />&nbsp;STANDARD<br />&nbsp;ACCELERATED|`withCondition("BudgetType = 'ACCELERATED'")`|Bing-specific filter
DeliveryStatus|Enumeration:<br />&nbsp;ELIGIBLE<br />&nbsp;LIMITED_BY_BUDGET<br />&nbsp;HOLD<br />&nbsp;CAMPAIGN_OUT_OF_BUDGET<br />&nbsp;CAMPAIGN_SUSPENDED<br />&nbsp;CAMPAIGN_PAUSED|`withCondition("DeliveryStatus NOT IN ['LIMITED_BY_BUDGET', 'HOLD', 'CAMPAIGN_OUT_OF_BUDGET']")`|Bing-specific filter
&nbsp;|&nbsp;|&nbsp;|&nbsp;

### Arguments:
|Name|Type|Description|
|-|-|-
condition|String|Condition to add to the selector.
### Returns:
|Type|Description|
|-|-
[CampaignSelector](./CampaignSelector)|Selector with the condition applied.

## <a name="withids~long-ids~"></a>withIds(long[] ids)
Returns a selector that will return only campaigns with the specified IDs.


The resulting selector can be further filtered by applying additional conditions to it.  All conditions will be 'AND' concatenated including any other ID based conditions.  For example:

```javascript
BingAdsApp.campaigns()
    .withIds([11111, 22222, 33333])
    .withIds([33333, 44444, 55555])
```

will only get the campaign with ID 33333 because it would be the only one satisfying both conditions.

The maximum number of IDs that you may specify is 1,000. If you specify more than 1,000 IDs, calling the get method will fail.
### Arguments:
|Name|Type|Description|
|-|-|-
ids|long[]|Array of campaign IDs.
### Returns:
|Type|Description|
|-|-
[CampaignSelector](./CampaignSelector)|Selector restricted to the given IDs.

