# ExpandedTextAdBuilder
Provides methods to define an expanded text ad.

Example usage:
```javascript
 var adOperation = adGroup.newAd().expandedTextAdBuilder()
    .withHeadlinePart1("First headline of ad")
    .withHeadlinePart2("Second headline of ad")
    .withDescription("Ad description")
    .withPath1("path1")
    .withPath2("path2")
    .withFinalUrl("http://www.contoso.com")
    .build();
 var ad = adOperation.getResult();
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[build](#build)|[AdOperation](./AdOperation)|Creates and returns an ad operation that can later be used to construct the new expanded text ad in the system.<br />
[withCustomParameters(String customParameters)](#withcustomparameters~string-customparameters~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the custom parameters for the new expanded text ad.
[withDescription(String description)](#withdescription~string-description~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the description of this new expanded text ad. <br />
[withFinalUrl(String finalUrl)](#withfinalurl~string-finalurl~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the final URL of this new expanded text to the specified value.<br />
[withHeadlinePart1(String headlinePart1)](#withheadlinepart1~string-headlinepart1~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the first part of the headline of this new expanded text ad to the specified value.<br />
[withHeadlinePart2(String headlinePart2)](#withheadlinepart2~string-headlinepart2~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the second part of the headline of this new expanded text ad to the specified value.<br />
[withMobileFinalUrl(String mobileFinalUrl)](#withmobilefinalurl~string-mobilefinalurl~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the mobile final URL of this new expanded text ad to the specified value.<br />
[withPath1(String path1)](#withpath1~string-path1~)|[ExpandedTextAdBuilder](ExpandedTextAdBuilder)|Sets the first path of the display URL of this new expanded text ad to the specified value.<br />
[withPath2(String path2)](#withpath2~string-path2~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the second path of the display URL of this new expanded text ad to the specified value.<br />
[withTrackingTemplate(String trackingTemplate)](#withtrackingtemplate~string-trackingtemplate~)|[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Sets the tracking template of this new expanded text ad to the specified value.<br />

## <a name="build"></a>build
Creates and returns an ad operation that can later be used to construct the new expanded text ad in the system.

### Returns:
|Type|Description|
|-|-
[AdOperation](./AdOperation)|Associated ad operation.

## <a name="withcustomparameters~string-customparameters~"></a>withCustomParameters(String customParameters)
Sets the custom parameters for the new expanded text ad. 

[!INCLUDE[custom-parameters](../includes/custom-parameters.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
customParameters|Object|Custom parameters of the ad as a map of the<br />        following form: <code>{key1: 'value1', key2: 'value2', key3: 'value3'}</code>.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified custom parameters.

## <a name="withdescription~string-description~"></a>withDescription(String description)
Sets the description of this new expanded text ad. 

### Arguments:
|Name|Type|Description|
|-|-|-
description|String|Ad description.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified description.

## <a name="withfinalurl~string-finalurl~"></a>withFinalUrl(String finalUrl)
Sets the final URL of this new expanded text to the specified value.


The final URL represents the actual landing page for your ad. The final URL must be the URL of the page that the user ends up on after clicking on your ad, once all the redirects have taken place.

Final URLs follow the same override rules as destination URLs. For example, a final URL at the keyword level overrides a final URL at an ad level.
### Arguments:
|Name|Type|Description|
|-|-|-
finalUrl|String|Final URL for the ad.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified final URL.

## <a name="withheadlinepart1~string-headlinepart1~"></a>withHeadlinePart1(String headlinePart1)
Sets the first part of the headline of this new expanded text ad to the specified value.

### Arguments:
|Name|Type|Description|
|-|-|-
headlinePart1|String|First part of the headline for the ad.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified first part of the headline.

## <a name="withheadlinepart2~string-headlinepart2~"></a>withHeadlinePart2(String headlinePart2)
Sets the second part of the headline of this new expanded text ad to the specified value.

### Arguments:
|Name|Type|Description|
|-|-|-
headlinePart2|String|Second part of the headline for the ad.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified second part of the headline.

## <a name="withmobilefinalurl~string-mobilefinalurl~"></a>withMobileFinalUrl(String mobileFinalUrl)
Sets the mobile final URL of this new expanded text ad to the specified value.


The mobile final URL represents the actual landing page for your ad on a mobile device. The final mobile URL must be the URL of the page that the user ends up on after clicking on your ad on a mobile device, once all the redirects have taken place.

Mobile final URLs follow the same override rules as destination URLs. For example, a mobile final URL at the keyword level overrides a mobile final URL at an ad level.
### Arguments:
|Name|Type|Description|
|-|-|-
mobileFinalUrl|String|Mobile final URL for the ad.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified final URL.

## <a name="withpath1~string-path1~"></a>withPath1(String path1)
Sets the first path of the display URL of this new expanded text ad to the specified value.

### Arguments:
|Name|Type|Description|
|-|-|-
urlPath1|String|Text of the first path.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](ExpandedTextAdBuilder)|Ad builder with the specified first URL path.

## <a name="withpath2~string-path2~"></a>withPath2(String path2)
Sets the second path of the display URL of this new expanded text ad to the specified value.

### Arguments:
|Name|Type|Description|
|-|-|-
urlPath2|String|Text of the second path.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified second URL path.

## <a name="withtrackingtemplate~string-trackingtemplate~"></a>withTrackingTemplate(String trackingTemplate)
Sets the tracking template of this new expanded text ad to the specified value.


[!INCLUDE[tracking-templates](../includes/tracking-templates.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
trackingTemplate|String|Tracking template for the ad.
### Returns:
|Type|Description|
|-|-
[ExpandedTextAdBuilder](./ExpandedTextAdBuilder)|Ad builder with the specified tracking template.

