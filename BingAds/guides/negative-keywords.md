---
title: "Negative Keywords"
ms.service: "bing-ads"
ms.topic: "article"
author: "eric-urban"
ms.author: "eur"
description: You can use negative keywords to prevent your ad from being displayed if the user's search query contains one of your negative keywords.
---
# Negative Keywords
A *negative keyword* is a specific word or phrase that helps to prevent your ad from being displayed to customers who are unlikely to click your ad. You can use negative keywords to prevent your ad from being displayed if the user's search query contains one of your negative keywords. The following types of comparisons are used to determine whether a negative keyword applies to the search query.

|Match Type|Description|
|--------------|---------------|
|Exact match|A match is prevented if all the words in the negative keyword exactly match the user's query.|
|Phrase match|Phrase match is the default match type. A match is prevented if all the words in the negative keyword are present somewhere in the user's query and are in the same order. For example, if your ad group contains "small red shoes" as a keyword and "sandals" as a negative keyword, searching for "small red sandals" would prevent a match because the query string contains the negative keyword, "sandals".|
For more information on when to use negative keywords see the Bing Ads help article, [Learn about using negative keywords to get to the right customers](http://help.bingads.microsoft.com/apex/index/3/en-us/51014).

You can [assign negative keywords](#assignednegativekeywords) to an individual campaign or ad group. If you specify negative keywords at both campaign and ad group levels, both sets of negative keywords will be in effect for the corresponding ad group. Negative keywords can also be added and deleted from a [shared negative keyword list](#sharednegativekeywordlists). The negative keyword list can be shared or associated with multiple campaigns. The negative keyword lists associated with a campaign are also effectively applied to all ad groups in the campaign. For example all negative keywords shown in the diagram below are applied to the Fall Sale ad group either directly or through inheritance from the campaign level associations. For other ad groups (not pictured) within the Shoe Sales campaign, the negative keywords sandals, thongs, flip flops, slides would not be in effect, unless those ad group also have the same negative keywords at ad group level.

![Two ways to add negative keywords](/bingads/guides/media/negative-keywords-structured.png "Two ways to add negative keywords")

For negative keyword limits per entity, please see [Negative Keywords](/bingads/guides/entity-hierarchy-limits#negativekeywords).

For code examples that show how to associate negative keywords and negative keyword lists with a campaign using the Campaign Management service, see [Negative Keywords Code Example](/bingads/guides/code-example-negative-keywords).

## <a name="assignednegativekeywords"></a>Assigned Negative Keywords
You may choose to assign a set of negative keywords to an individual campaign or ad group. An assigned set of negative keywords cannot be shared with other campaigns or ad groups. You can manage an assigned set of negative keywords with the [AddNegativeKeywordsToEntities](/binga/bingads/campaign-management-service/addnegativekeywordstoentities), [DeleteNegativeKeywordsFromEntities](/binga/bingads/campaign-management-service/deletenegativekeywordsfromentities), and [GetNegativeKeywordsByEntityIds](/binga/bingads/campaign-management-service/getnegativekeywordsbyentityids) operations.

A [NegativeKeyword](/binga/bingads/campaign-management-service/negativekeyword) cannot be updated. To make an update, for example to change the match type of an existing negative keyword you must first pass the existing [NegativeKeyword](/binga/bingads/campaign-management-service/negativekeyword) to [DeleteNegativeKeywordsFromEntities](/binga/bingads/campaign-management-service/deletenegativekeywordsfromentities), and then call [AddNegativeKeywordsToEntities](/binga/bingads/campaign-management-service/addnegativekeywordstoentities) with the desired match type for a new [NegativeKeyword](/binga/bingads/campaign-management-service/negativekeyword) instance.

## <a name="sharednegativekeywordlists"></a>Shared Negative Keyword Lists
Negative keywords can be added and deleted from a shared negative keyword list. The negative keyword list can be shared or associated with multiple campaigns.

> [!NOTE]
> Negative keyword lists cannot be associated with an ad group. An ad group can only be assigned an exclusive set of negative keywords. In addition to the exclusive set of negative keywords that can be assigned to a campaign, each campaign can be associated with one negative keyword list.

To create a negative keyword list, call the [AddSharedEntity](/binga/bingads/campaign-management-service/addsharedentity) operation and pass a [NegativeKeywordList](/binga/bingads/campaign-management-service/negativekeywordlist), which inherits from both [SharedList](/binga/bingads/campaign-management-service/sharedlist) and [SharedEntity](/binga/bingads/campaign-management-service/sharedentity). You can create up to 20 negative keyword lists per account and share or associate them with any campaign in the same account. You can get existing negative keyword lists by calling the [GetSharedEntitiesByAccountId](/binga/bingads/campaign-management-service/getsharedentitiesbyaccountid) operation. You can update the name of the negative keyword list by calling the [UpdateSharedEntities](/binga/bingads/campaign-management-service/updatesharedentities) operation. You can delete the negative keyword list by calling the [DeleteSharedEntities](/binga/bingads/campaign-management-service/deletesharedentities) operation.

To add negative keywords to a negative keyword list, call the [AddListItemsToSharedList](/binga/bingads/campaign-management-service/addlistitemstosharedlist) operation and pass a list of [NegativeKeyword](/binga/bingads/campaign-management-service/negativekeyword), which inherits from [SharedListItem](/binga/bingads/campaign-management-service/sharedlistitem). You can add up to 5,000 negative keywords to each negative keyword list. You can get negative keywords within a specified list by calling the [GetListItemsBySharedList](/binga/bingads/campaign-management-service/getlistitemsbysharedlist) operation. Negative keywords can be removed from a list by calling the [DeleteListItemsFromSharedList](/binga/bingads/campaign-management-service/deletelistitemsfromsharedlist) operation.

A [NegativeKeyword](/binga/bingads/campaign-management-service/negativekeyword) cannot be updated. To make an update, for example to change the match type of an existing negative keyword you must first pass the existing [NegativeKeyword](/binga/bingads/campaign-management-service/negativekeyword) to [DeleteListItemsFromSharedList](/binga/bingads/campaign-management-service/deletelistitemsfromsharedlist), and then call [AddListItemsToSharedList](/binga/bingads/campaign-management-service/addlistitemstosharedlist) with the desired match type for a new [NegativeKeyword](/binga/bingads/campaign-management-service/negativekeyword) instance.

To associate a negative keyword list with a campaign, specify an array of [SharedEntityAssociation](/binga/bingads/campaign-management-service/sharedentityassociation) with the [SetSharedEntityAssociations](/binga/bingads/campaign-management-service/setsharedentityassociations) service operation. Each [SharedEntityAssociation](/binga/bingads/campaign-management-service/sharedentityassociation) should include the type of entity (currently only Campaign is supported), campaign identifier, and negative keyword list identifier. You can get the associations by entity identifier or negative keyword list identifier by calling the respective [GetSharedEntityAssociationsByEntityIds](/binga/bingads/campaign-management-service/getsharedentityassociationsbyentityids) and [GetSharedEntityAssociationsBySharedEntityIds](/binga/bingads/campaign-management-service/getsharedentityassociationsbysharedentityids) operations. You can remove the association between the campaign and negative keyword list by calling the [DeleteSharedEntityAssociations](/binga/bingads/campaign-management-service/deletesharedentityassociations) operation.

## Find Conflicts between Your Negative Keywords and Keywords
The reporting service provides a negative-keyword conflict report that lists the negative keywords that you also specify as keywords. Specifying a negative keyword that is also a keyword negates the keyword. For more information, see the [NegativeKeywordConflictReportRequest](/binga/bingads/reporting-service/negativekeywordconflictreportrequest) request.

## See Also
[Bing Ads Web Service Addresses](/bingads/guides/web-service-addresses)

