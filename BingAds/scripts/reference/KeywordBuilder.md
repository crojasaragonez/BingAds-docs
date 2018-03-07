# KeywordBuilder
Provides methods for defining and building a keyword.

Example usage:
```javascript
 var keywordOperation = adGroup.newKeywordBuilder()
    .withText("text")
    .withCpc(1.5)
    .withFinalUrl("http://www.example.com")
    .build();
 var keyword = keywordOperation.getResult();
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[build](#build)|[KeywordOperation](./KeywordOperation)|Returns a keyword operation with the defined properties which can later be used to construct the keyword.<br />
[withCpc(double cpc)](#withcpc~double-cpc~)|[KeywordBuilder](./KeywordBuilder)|Returns a keyword builder with the CPC property set to the specified value.<br />
[withCustomParameters( String customParameters)](#withcustomparameters~-string-customparameters~)|[KeywordBuilder](./KeywordBuilder)|Returns a keyword builder with the custom parameters set to the specified value.
[withFinalUrl(String finalUrl)](#withfinalurl~string-finalurl~)|[KeywordBuilder](./KeywordBuilder)|Returns a keyword builder with the final URL set to the specified value.<br />
[withMobileFinalUrl(String mobileFinalUrl)](#withmobilefinalurl~string-mobilefinalurl~)|[KeywordBuilder](./KeywordBuilder)|Returns a keyword builder with the mobile final URL set to the specified value.<br />
[withText(String text)](#withtext~string-text~)|[KeywordBuilder](./KeywordBuilder)|Returns a keyword builder with the text set to the specified value.      <br />
[withTrackingTemplate( String trackingTemplate)](#withtrackingtemplate~-string-trackingtemplate~)|[KeywordBuilder](./KeywordBuilder)|Returns a keyword builder with the tracking template set to the specified value.<br />

## <a name="build"></a>build
Returns a keyword operation with the defined properties which can later be used to construct the keyword.

### Returns:
|Type|Description|
|-|-
[KeywordOperation](./KeywordOperation)|The associated keyword operation.

## <a name="withcpc~double-cpc~"></a>withCpc(double cpc)
Returns a keyword builder with the CPC property set to the specified value.

### Arguments:
|Name|Type|Description|
|-|-|-
cpc|double|The max CPC bid of the keyword.
### Returns:
|Type|Description|
|-|-
[KeywordBuilder](./KeywordBuilder)|The keyword builder with the specified max CPC.

## <a name="withcustomparameters~-string-customparameters~"></a>withCustomParameters( String customParameters)
Returns a keyword builder with the custom parameters set to the specified value.

Customer parameter names may contain only alphanumeric characters and must not exceed 16 bytes. When you include custom parameters in final URLs and tracking templates, the convention is to prefix the parameter's name with an underscore and enclose the parameter in curly braces ({}). For example, {_param}.  Custom parameter values may not contain whitespace and must not exceed 200 bytes.

If an ad group does not specify custom parameters, it inherits them from its parent campaign. Likewise, ads in the ad group inherit the parameters from the ad group if the ad does not specify its own parameters. 

For more information, see [Custom Parameters](/bingads/guides/url-tracking-upgraded-urls#customparametersvalidation).
### Arguments:
|Name|Type|Description|
|-|-|-
customParameters|Object|The custom parameters of the keyword as a map of the<br />        following form: <code>{key1: 'value1', key2: 'value2', key3: 'value3'}</code>.
### Returns:
|Type|Description|
|-|-
[KeywordBuilder](./KeywordBuilder)|The keyword builder with the specified custom parameters.

## <a name="withfinalurl~string-finalurl~"></a>withFinalUrl(String finalUrl)
Returns a keyword builder with the final URL set to the specified value.


The final URL represents the actual landing page for your ad. The final URL must be the URL of the page that the user ends up on after clicking on your ad, once all the redirects have taken place.

Final URLs follow the same override rules as destination URLs. For example, a final URL at the keyword level overrides a final URL at an ad level.
### Arguments:
|Name|Type|Description|
|-|-|-
finalUrl|String|The final URL for the keyword.
### Returns:
|Type|Description|
|-|-
[KeywordBuilder](./KeywordBuilder)|The keyword builder with the specified final URL.

## <a name="withmobilefinalurl~string-mobilefinalurl~"></a>withMobileFinalUrl(String mobileFinalUrl)
Returns a keyword builder with the mobile final URL set to the specified value.


The mobile final URL represents the actual landing page for your ad on a mobile device. The final mobile URL must be the URL of the page that the user ends up on after clicking on your ad on a mobile device, once all the redirects have taken place.

Mobile final URLs follow the same override rules as destination URLs. For example, a mobile final URL at the keyword level overrides a mobile final URL at an ad level.
### Arguments:
|Name|Type|Description|
|-|-|-
mobileFinalUrl|String|The mobile final URL for the keyword.
### Returns:
|Type|Description|
|-|-
[KeywordBuilder](./KeywordBuilder)|The keyword builder with the specified final URL.

## <a name="withtext~string-text~"></a>withText(String text)
Returns a keyword builder with the text set to the specified value.      


To specify match type for the new keyword:

- `keywordBuilder.withText("books")` - broad match.
- `keywordBuilder.withText("\"books\"")` - phrase match.
- `keywordBuilder.withText("[hardcover books]")` - exact match.

### Arguments:
|Name|Type|Description|
|-|-|-
text|String|The text of the keyword.
### Returns:
|Type|Description|
|-|-
[KeywordBuilder](./KeywordBuilder)|Keyword builder with the specified text.

## <a name="withtrackingtemplate~-string-trackingtemplate~"></a>withTrackingTemplate( String trackingTemplate)
Returns a keyword builder with the tracking template set to the specified value.


You can optionally use the tracking template to specify additional tracking parameters or redirects. Bing Ads will use this template to assemble the actual destination URL to associate with the ad.

A tracking template specified at a lower level entity will override the setting specified at a higher level entity, for example, a tracking template at the ad group level overrides the setting at the campaign level.
### Arguments:
|Name|Type|Description|
|-|-|-
trackingTemplate|String|The tracking template for the keyword.
### Returns:
|Type|Description|
|-|-
[KeywordBuilder](./KeywordBuilder)|The keyword builder with the specified tracking template.

