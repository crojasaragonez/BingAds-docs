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
[isPaused](#ispaused)|boolean|Returns true if this campaign is enabled <br />
[isRemoved](#isremoved)|boolean|Returns true if this campaign is removed. <br />
[pause](#pause)|void|Pauses this campaign.<br />
[remove](#remove)|void|Remove the campaign.<br />
[setName(String name)](#setname~string-name~)|void|Sets the name of this campaign.<br />
[urls](#urls)|[CampaignUrls](./CampaignUrls)|Returns the URL fields of this campaign.<br />
&nbsp;|&nbsp;|&nbsp;

## <a name="addnegativekeywordlist~negativekeywordlist-negativekeywordlist~"></a>addNegativeKeywordList(NegativeKeywordList negativeKeywordList)
Adds a negative keyword list to the campaign.



### Arguments:
|Name|Type|Description|
|-|-|-
negativeKeywordList|[NegativeKeywordList](./NegativeKeywordList)|The negative keyword list to add to the campaign.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="enable"></a>enable
Enables this campaign.

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
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
String|The type of the campaign's bidding strategy.
&nbsp;|&nbsp;
## <a name="getbudget"></a>getBudget
Returns the budget for this campaign.

### Returns:
|Type|Description|
|-|-
[Budget](./Budget)|The budget for this campaign.
&nbsp;|&nbsp;
## <a name="getentitytype"></a>getEntityType
Returns the entity type of this campaign, which is "Campaign".

### Returns:
|Type|Description|
|-|-
String|The entity type of this campaign, which is "Campaign".
&nbsp;|&nbsp;
## <a name="getid"></a>getId
Returns the ID of this campaign.

### Returns:
|Type|Description|
|-|-
long|The ID of this campaign.
&nbsp;|&nbsp;
## <a name="getname"></a>getName
Returns the name of this campaign.

### Returns:
|Type|Description|
|-|-
String|The name of this campaign.
&nbsp;|&nbsp;
## <a name="ispaused"></a>isPaused
Returns true if this campaign is enabled 

### Returns:
|Type|Description|
|-|-
boolean|True if this campaign is paused.
&nbsp;|&nbsp;
## <a name="isremoved"></a>isRemoved
Returns true if this campaign is removed. 

### Returns:
|Type|Description|
|-|-
boolean|True if this campaign is removed.
&nbsp;|&nbsp;
## <a name="pause"></a>pause
Pauses this campaign.

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="remove"></a>remove
Remove the campaign.

### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="setname~string-name~"></a>setName(String name)
Sets the name of this campaign.

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The new name for the campaign.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="urls"></a>urls
Returns the URL fields of this campaign.

### Returns:
|Type|Description|
|-|-
[CampaignUrls](./CampaignUrls)|The URL fields of this campaign.
&nbsp;|&nbsp;
