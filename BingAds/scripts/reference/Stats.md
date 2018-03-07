# Stats
Provides statistics related to the different entity types.

Example usage:
```javascript
 var stats = campaign.getStatsFor("LAST_MONTH");
 var impressions = stats.getImpressions();
 var clicks = stats.getClicks();
 // etc.
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[getAverageCpc](#getaveragecpc)|double|Returns the average cost per click of the associated entity.<br />
[getAveragePosition](#getaverageposition)|double|Returns the average position of the associated entity.<br />
[getClicks](#getclicks)|long|Returns the number of clicks of the associated entity.<br />
[getCost](#getcost)|double|Returns the cost (spend) of the associated entity in the currency of the current account.<br />
[getCtr](#getctr)|double|Returns the calick through rate of the associated entity within the 0..1 range. <br />
[getImpressions](#getimpressions)|long|Returns the number of impressions of the associated entity.<br />

## <a name="getaveragecpc"></a>getAverageCpc
Returns the average cost per click of the associated entity.

### Returns:
|Type|Description|
|-|-
double|Average cost per click.

## <a name="getaverageposition"></a>getAveragePosition
Returns the average position of the associated entity.

### Returns:
|Type|Description|
|-|-
double|Average position.

## <a name="getclicks"></a>getClicks
Returns the number of clicks of the associated entity.

### Returns:
|Type|Description|
|-|-
long|Number of clicks.

## <a name="getcost"></a>getCost
Returns the cost (spend) of the associated entity in the currency of the current account.

### Returns:
|Type|Description|
|-|-
double|Cost in the default currency of the account.

## <a name="getctr"></a>getCtr
Returns the calick through rate of the associated entity within the 0..1 range. 

### Returns:
|Type|Description|
|-|-
double|Click through rate.

## <a name="getimpressions"></a>getImpressions
Returns the number of impressions of the associated entity.

### Returns:
|Type|Description|
|-|-
long|Number of impressions.

