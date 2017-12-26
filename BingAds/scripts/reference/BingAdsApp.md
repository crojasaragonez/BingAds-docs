# BingAdsApp
This is the root object of the Bing Ads Scripts API. It provides methods to retrieve different types of Bing Ads entities for the current Bing Ads account.
# Methods
|Method Name|Return Type|Description|
|-|-|-
[adGroups](#adgroups)|[AdGroupSelector](./AdGroupSelector)|Returns a selector of all ad groups in the current account.<br />
[campaigns](#campaigns)|[CampaignSelector](./CampaignSelector)|Returns a selector of all campaigns in the current account.<br />
[keywords](#keywords)|[KeywordSelector](./KeywordSelector)|Returns a selector of all keywords in the current account.<br />
[negativeKeywordList](#negativekeywordlist)|[NegativeKeywordListSelector](./NegativeKeywordListSelector)|Returns a selector of all negative keyword lists in this account.
[newNegativeKeywordListBuilder](#newnegativekeywordlistbuilder)|[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|Returns a new negative keyword list builder for the current account. The new negative keyword list is created when builder.build() is called.<br />
&nbsp;|&nbsp;|&nbsp;

## <a name="adgroups"></a>adGroups
Returns a selector of all ad groups in the current account.




### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|The selector of all ad groups in the current account.
&nbsp;|&nbsp;
## <a name="campaigns"></a>campaigns
Returns a selector of all campaigns in the current account.


Example:
```javascript
var campaignSelector = BingAdsApp.campaigns();
```

### Returns:
|Type|Description|
|-|-
[CampaignSelector](./CampaignSelector)|Selector of all campaigns that share this budget.
&nbsp;|&nbsp;
## <a name="keywords"></a>keywords
Returns a selector of all keywords in the current account.

### Returns:
|Type|Description|
|-|-
[KeywordSelector](./KeywordSelector)|Selector of all keywords in the current account.
&nbsp;|&nbsp;
## <a name="negativekeywordlist"></a>negativeKeywordList
Returns a selector of all negative keyword lists in this account.



### Returns:
|Type|Description|
|-|-
[NegativeKeywordListSelector](./NegativeKeywordListSelector)|A selector of all negative keyword lists in this account.
&nbsp;|&nbsp;
## <a name="newnegativekeywordlistbuilder"></a>newNegativeKeywordListBuilder
Returns a new negative keyword list builder for the current account. The new negative keyword list is created when builder.build() is called.




### Returns:
|Type|Description|
|-|-
[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|The negative keyword list builder used to create a new negative keyword list in the current account.
&nbsp;|&nbsp;
