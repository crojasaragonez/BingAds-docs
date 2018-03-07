# AdGroupBuilder
Provides methods which can be used to define and build an ad group.

Example usage:
```javascript
 var adGroupBuilder = campaign.newAdGroupBuilder();
 var adGroupOperation = adGroupBuilder
    .withName("ad group name")
    .withStatus("PAUSED")
    .build();
 var adGroup = adGroupOperation.getResult();
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[build](#build)|[AdGroupOperation](./AdGroupOperation)|Returns an ad group operation which represents the ad group to be created.<br />
[withBiddingStrategy(String biddingStrategy)](#withbiddingstrategy~string-biddingstrategy~)|[AdGroupBuilder](./AdGroupBuilder)|Sets the ad group's bidding strategy.<br />
[withCpc(double cpc)](#withcpc~double-cpc~)|[AdGroupBuilder](./AdGroupBuilder)|Sets the maximum CPC bid to be used for this new ad group.<br />
[withCustomParameters(Object customParams)](#withcustomparameters~object-customparams~)|[AdGroupBuilder](./AdGroupBuilder)|Sets the custom parameters for the new ad group.
[withName(String name)](#withname~string-name~)|[AdGroupBuilder](./AdGroupBuilder)|Sets the name of this ad group. <br />
[withStatus(String status)](#withstatus~string-status~)|[AdGroupBuilder](./AdGroupBuilder)|Sets the status of this new ad group to the provided value.<br />
[withTrackingTemplate(String trackingTemplate)](#withtrackingtemplate~string-trackingtemplate~)|[AdGroupBuilder](./AdGroupBuilder)|Sets the tracking template of this ad group.<br />

## <a name="build"></a>build
Returns an ad group operation which represents the ad group to be created.

### Returns:
|Type|Description|
|-|-
[AdGroupOperation](./AdGroupOperation)|The associated ad group operation.

## <a name="withbiddingstrategy~string-biddingstrategy~"></a>withBiddingStrategy(String biddingStrategy)
Sets the ad group's bidding strategy.





### Arguments:
|Name|Type|Description|
|-|-|-
biddingStrategy|String|The bidding strategy of the ad group. Possible values are:<br />
- MANUAL_CPC
### Returns:
|Type|Description|
|-|-
[AdGroupBuilder](./AdGroupBuilder)|The ad group builder with the specified bidding strategy.

## <a name="withcpc~double-cpc~"></a>withCpc(double cpc)
Sets the maximum CPC bid to be used for this new ad group.



### Arguments:
|Name|Type|Description|
|-|-|-
cpc|double|The max CPC bid of the ad group. If no CPC is specified, the default of 0.30 is used.<br />
### Returns:
|Type|Description|
|-|-
[AdGroupBuilder](./AdGroupBuilder)|The ad group builder with the specified max CPC.

## <a name="withcustomparameters~object-customparams~"></a>withCustomParameters(Object customParams)
Sets the custom parameters for the new ad group.

[!INCLUDE[custom-parameters](../includes/custom-parameters.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
customParameters|Object|The custom parameters of the ad group as a map of the following form: <code>{key1: 'value1', key2: 'value2', key3: 'value3'}</code>.
### Returns:
|Type|Description|
|-|-
[AdGroupBuilder](./AdGroupBuilder)|An ad group builder with the customer parameters applied.

## <a name="withname~string-name~"></a>withName(String name)
Sets the name of this ad group. 

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The ad group's name. The string can contain a maximum of 256 characters, and must be unique among all active ad groups within the campaign.
### Returns:
|Type|Description|
|-|-
[AdGroupBuilder](./AdGroupBuilder)|An ad group builder with the name applied.

## <a name="withstatus~string-status~"></a>withStatus(String status)
Sets the status of this new ad group to the provided value.


If no value is specified, it will default to `ENABLED`.
### Arguments:
|Name|Type|Description|
|-|-|-
status|String|Ad group status.
### Returns:
|Type|Description|
|-|-
[AdGroupBuilder](./AdGroupBuilder)|Ad group builder with the specified status.

## <a name="withtrackingtemplate~string-trackingtemplate~"></a>withTrackingTemplate(String trackingTemplate)
Sets the tracking template of this ad group.


[!INCLUDE[tracking-templates](../includes/tracking-templates.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
trackingTemplate|String|The tracking template for the ad group.
### Returns:
|Type|Description|
|-|-
[AdGroupBuilder](./AdGroupBuilder)|An ad group builder with the tracking template applied.

