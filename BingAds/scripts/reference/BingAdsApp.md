# BingAdsApp
This is the root object of the Bing Ads Scripts API. It provides methods to access different entities such as campaigns and keywords for a single Bing Ads account.
# Methods
|Method Name|Return Type|Description|
|-|-|-
[adGroups](#adgroups)|[AdGroupSelector](./AdGroupSelector)|Returns a selector of all ad groups in this account.<br />
[campaigns](#campaigns)|[CampaignSelector](./CampaignSelector)|Returns a selector of all campaigns in this account.<br />
[keywords](#keywords)|[KeywordSelector](./KeywordSelector)|Returns a selector of all keywords in this account.<br />
[negativeKeywordList](#negativekeywordlist)|[NegativeKeywordListSelector](./NegativeKeywordListSelector)|Returns a selector of all negative keyword lists in this account.
[newNegativeKeywordListBuilder](#newnegativekeywordlistbuilder)|[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|Returns a new negative keyword list builder for this account. <br />

## <a name="adgroups"></a>adGroups
Returns a selector of all ad groups in this account.



### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|Selector of all ad groups in the current account.

## <a name="campaigns"></a>campaigns
Returns a selector of all campaigns in this account.



### Returns:
|Type|Description|
|-|-
[CampaignSelector](./CampaignSelector)|Selector of all campaigns that share this budget.

## <a name="keywords"></a>keywords
Returns a selector of all keywords in this account.

### Returns:
|Type|Description|
|-|-
[KeywordSelector](./KeywordSelector)|Selector of all keywords in the current account.

## <a name="negativekeywordlist"></a>negativeKeywordList
Returns a selector of all negative keyword lists in this account.


### Returns:
|Type|Description|
|-|-
[NegativeKeywordListSelector](./NegativeKeywordListSelector)|Selector of all negative keyword lists in this account.

## <a name="newnegativekeywordlistbuilder"></a>newNegativeKeywordListBuilder
Returns a new negative keyword list builder for this account. 


The new negative keyword list is created when builder.build() is called.
### Returns:
|Type|Description|
|-|-
[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|New negative keyword list builder for the current account.

