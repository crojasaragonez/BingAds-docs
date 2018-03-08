# Campaign
Represents a campaign.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[addNegativeKeywordList(NegativeKeywordList negativeKeywordList)](#addnegativekeywordlist~negativekeywordlist-negativekeywordlist~)|void|Adds a negative keyword list to the campaign.
[enable](#enable)|void|Enables this campaign.<br />
[getBiddingStrategyType](#getbiddingstrategytype)|String|Returns the type of the campaign's bidding strategy.<br />
[getBudget](#getbudget)|[Budget](./Budget)|Returns the budget for this campaign.<br />
[getEntityType](#getentitytype)|String|Returns the entity type of this campaign, which is "Campaign".<br />
[getId](#getid)|long|Returns the ID of this campaign.<br />
[getName](#getname)|String|Returns the name of this campaign.<br />
[isPaused](#ispaused)|boolean|Returns a boolean value that determines if this campaign is paused.
[isRemoved](#isremoved)|boolean|Returns a boolean value that determines if this campaign is removed.
[pause](#pause)|void|Pauses this campaign.<br />
[remove](#remove)|void|Remove the campaign.<br />
[setName(String name)](#setname~string-name~)|void|Sets the name of this campaign.<br />
[urls](#urls)|[CampaignUrls](./CampaignUrls)|Returns the URL fields of this campaign.<br />

## <a name="addnegativekeywordlist~negativekeywordlist-negativekeywordlist~"></a>addNegativeKeywordList(NegativeKeywordList negativeKeywordList)
Adds a negative keyword list to the campaign.


### Arguments:
|Name|Type|Description|
|-|-|-
negativeKeywordList|[NegativeKeywordList](./NegativeKeywordList)|Negative keyword list to add to the campaign.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="enable"></a>enable
Enables this campaign.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="getbiddingstrategytype"></a>getBiddingStrategyType
Returns the type of the campaign's bidding strategy.


Possible return values are:

- MANUAL_CPC
- MANUAL_CPM
- BUDGET_OPTIMIZER
- CONVERSION_OPTIMIZER
- PERCENT_CPA

### Returns:
|Type|Description|
|-|-
String|Type of the campaign's bidding strategy.

## <a name="getbudget"></a>getBudget
Returns the budget for this campaign.

### Returns:
|Type|Description|
|-|-
[Budget](./Budget)|Budget for this campaign.

## <a name="getentitytype"></a>getEntityType
Returns the entity type of this campaign, which is "Campaign".

### Returns:
|Type|Description|
|-|-
String|Entity type of this campaign, which is "Campaign".

## <a name="getid"></a>getId
Returns the ID of this campaign.

### Returns:
|Type|Description|
|-|-
long|ID of this campaign.

## <a name="getname"></a>getName
Returns the name of this campaign.

### Returns:
|Type|Description|
|-|-
String|Name of this campaign.

## <a name="ispaused"></a>isPaused
Returns a boolean value that determines if this campaign is paused.
### Returns:
|Type|Description|
|-|-
boolean|Boolean value that determines if this campaign is paused.

## <a name="isremoved"></a>isRemoved
Returns a boolean value that determines if this campaign is removed.
### Returns:
|Type|Description|
|-|-
boolean|Boolean value that determines if this campaign is removed.

## <a name="pause"></a>pause
Pauses this campaign.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="remove"></a>remove
Remove the campaign.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="setname~string-name~"></a>setName(String name)
Sets the name of this campaign.

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|New name for the campaign.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="urls"></a>urls
Returns the URL fields of this campaign.

### Returns:
|Type|Description|
|-|-
[CampaignUrls](./CampaignUrls)|URL fields of this campaign.

