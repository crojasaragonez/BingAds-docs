---
title: "Dynamic Search Ads"
ms.service: "bing-ads"
ms.topic: "article"
author: "eric-urban"
ms.author: "eur"
description: Setup Dynamic Search ads with the Bing Ads API.
---
# Dynamic Search Ads
Dynamic Search Ads are coming to Bing Ads. You will be able to create a new type of campaign where the ad copy is automatically generated from the content on your website. 

> [!NOTE]
> Not everyone has this feature yet. If you don't, don't worry. It's coming soon.
> 
> Before you can use dynamic search ads, you must upgrade to Final Urls. For more information, see [URL Tracking with Upgraded URLs](/bingads/guides/url-tracking-upgraded-urls).

## <a name="bulk"></a>Bulk API for Dynamic Search Ads  
The following Bulk records are available for managing dynamic search ads campaigns.
* [Ad Group Dynamic Search Ad Target](/binga/bingads/bulk-service/ad-group-dynamic-search-ad-target)
* [Ad Group Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/ad-group-negative-dynamic-search-ad-target)
* [Campaign Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/campaign-negative-dynamic-search-ad-target)
* [Dynamic Search Ad](/binga/bingads/bulk-service/dynamic-search-ad)
 
To get started with dynamic search ads, first you'll need to define a [Campaign](/binga/bingads/bulk-service/campaign) record with the *Campaign Type* field set to *DynamicSearchAds*. When you create the campaign, you'll also need to specify the *Domain Language* and *Website* fields.  

Next, define an [Ad Group](/binga/bingads/bulk-service/ad-group) within the dynamic search ads campaign. You can add one or more [Ad Group Dynamic Search Ad Target](/binga/bingads/bulk-service/ad-group-dynamic-search-ad-target) records for the parent ad group that helps determine whether or not to serve dynamic search ads. 

If you want to exclude certain portions of your website, you can add negative targets at the campaign and/or ad group level using the respective [Campaign Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/campaign-negative-dynamic-search-ad-target) and [Ad Group Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/ad-group-negative-dynamic-search-ad-target) records. The [Campaign Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/campaign-negative-dynamic-search-ad-target) at the campaign level applies to all ad groups within the campaign; however, if you define ad group level [Ad Group Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/ad-group-negative-dynamic-search-ad-target), the campaign target is ignored for that ad group. 

For any of the [Ad Group Dynamic Search Ad Target](/binga/bingads/bulk-service/ad-group-dynamic-search-ad-target), [Ad Group Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/ad-group-negative-dynamic-search-ad-target), and [Campaign Negative Dynamic Search Ad Target](/binga/bingads/bulk-service/campaign-negative-dynamic-search-ad-target) records, you can choose whether you want the target argument to match partial URLs, page content, page title, or categories that Bing thinks applies to your website. To discover the categories that you can use for targets (positive or negative), call the [GetDomainCategories](/binga/bingads/ad-insight-service/getdomaincategories) operation with the Ad Insight service.

Finally you can define a [Dynamic Search Ad](/binga/bingads/bulk-service/dynamic-search-ad) record assigned to the ad group. The ad title and display URL are generated automatically based on the website domain and language that you want to target.


## <a name="campaign"></a>Campaign Management API for Dynamic Search Ads  

To get started with dynamic search ads, first you'll need to [add](/binga/bingads/campaign-management-service/addcampaigns) a new [Campaign](/binga/bingads/campaign-management-service/campaign) with its type set to *DynamicSearchAds*. When you create the campaign, you'll need to include a [DynamicSearchAdsSetting](/binga/bingads/campaign-management-service/dynamicsearchadssetting) that specifies the target website domain and language. The new *DynamicSearchAds* value is added to the [CampaignType](/binga/bingads/campaign-management-service/campaigntype) value set. 

Next, [create](/binga/bingads/campaign-management-service/addadgroups) a new [AdGroup](/binga/bingads/campaign-management-service/adgroup) within the dynamic search ads campaign. You can add one or more [Webpage](/binga/bingads/campaign-management-service/webpage) criterion to each ad group that helps determine whether or not to serve dynamic search ads, by calling the [AddAdGroupCriterions](/binga/bingads/campaign-management-service/addadgroupcriterions) operation. 

If you want to exclude certain portions of your website, you can add negative [Webpage](/binga/bingads/campaign-management-service/webpage) criterion at the campaign and/or ad group level using the respective [AddCampaignCriterions](/binga/bingads/campaign-management-service/addcampaigncriterions) and [AddAdGroupCriterions](/binga/bingads/campaign-management-service/addadgroupcriterions) service operations. The negative [Webpage](/binga/bingads/campaign-management-service/webpage) criterion at the campaign level applies to all ad groups within the campaign; however, if you define ad group level negative [Webpage](/binga/bingads/campaign-management-service/webpage) criterion, the campaign criterion is ignored for that ad group. 

Whether the criterion is positive or negative, you can choose whether you want the criterion argument to match partial URLs, page content, page title, or categories that Bing thinks applies to your website. To discover the categories that you can use for [Webpage](/binga/bingads/campaign-management-service/webpage) criterion (positive or negative), use the [GetDomainCategories](/binga/bingads/ad-insight-service/getdomaincategories) operation with the Ad Insight service.

Finally you can [add](/binga/bingads/campaign-management-service/addads) a [DynamicSearchAd](/binga/bingads/campaign-management-service/dynamicsearchad) into the ad group. The ad title and display URL are generated automatically based on the website domain and language that you want to target.
