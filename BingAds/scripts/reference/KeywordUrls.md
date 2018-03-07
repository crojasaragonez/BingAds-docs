# KeywordUrls
Provides access to the URLs for this keyword.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[clearTrackingTemplate](#cleartrackingtemplate)|void|Clears the tracking template of this keyword.<br />
[getCustomParameters](#getcustomparameters)|Object|Returns the custom parameters of this keyword.
[getFinalUrl](#getfinalurl)|String|Returns the final URL of this keyword.<br />
[getTrackingTemplate](#gettrackingtemplate)|String|Returns the tracking template of this keyword.<br />
[setCustomParameters(Object customParameters)](#setcustomparameters~object-customparameters~)|void|Sets the custom parameters of this keyword.
[setFinalUrl(String finalUrl)](#setfinalurl~string-finalurl~)|void|Sets the final URL of this keyword.<br />
[setTrackingTemplate(String trackingTemplate)](#settrackingtemplate~string-trackingtemplate~)|void|Sets the tracking template of this keyword.<br />

## <a name="cleartrackingtemplate"></a>clearTrackingTemplate
Clears the tracking template of this keyword.


If you clear the tracking template specified at a lower level entity (for example, a keyword), and you have also specified tracking template on a higher level entity, (for example, the parent ad group), then Bing Ads will use the tracking template specified at the higher level entity (the ad group level tracking template will be used). To completely clear the tracking template, it must be cleared at all levels of the hierarchy at which it was set.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="getcustomparameters"></a>getCustomParameters
Returns the custom parameters of this keyword.

An ad group may specify up to three custom parameters. Customer parameter names may contain only alphanumeric characters and must not exceed 16 bytes. When you include custom parameters in final URLs and tracking templates, the convention is to prefix the parameter's name with an underscore and enclose the parameter in curly braces ({}). For example, {_param}.  Custom parameter values may not contain whitespace and must not exceed 200 bytes.

If an ad group does not specify custom parameters, it inherits them from its parent campaign. Likewise, ads in the ad group inherit the parameters from the ad group if the ad does not specify its own parameters. 

For more information, see [Custom Parameters](/bingads/guides/url-tracking-upgraded-urls#customparametersvalidation).
### Returns:
|Type|Description|
|-|-
Object|The custom parameters of the keyword as a map of the following form: {key1: 'value1', key2: 'value2', key3: 'value3'}.

## <a name="getfinalurl"></a>getFinalUrl
Returns the final URL of this keyword.


The final URL represents the actual landing page for your ad. The final URL must be the URL of the page that the user ends up on after clicking on your ad, once all the redirects have taken place.

Final URLs follow the same override rules as destination URLs. For example, a final URL at the keyword level overrides a final URL at an ad level.
### Returns:
|Type|Description|
|-|-
String|The final URL of the keyword.

## <a name="gettrackingtemplate"></a>getTrackingTemplate
Returns the tracking template of this keyword.


You can optionally use the tracking template to specify additional tracking parameters or redirects. Bing Ads will use this template to assemble the actual destination URL to associate with the ad.

A tracking template specified at a lower level entity will override the setting specified at a higher level entity, for example, a tracking template at the ad group level overrides the setting at the campaign level.
### Returns:
|Type|Description|
|-|-
String|The tracking template of the keyword.

## <a name="setcustomparameters~object-customparameters~"></a>setCustomParameters(Object customParameters)
Sets the custom parameters of this keyword.

An ad group may specify up to three custom parameters. Customer parameter names may contain only alphanumeric characters and must not exceed 16 bytes. When you include custom parameters in final URLs and tracking templates, the convention is to prefix the parameter's name with an underscore and enclose the parameter in curly braces ({}). For example, {_param}.  Custom parameter values may not contain whitespace and must not exceed 200 bytes.

If an ad group does not specify custom parameters, it inherits them from its parent campaign. Likewise, ads in the ad group inherit the parameters from the ad group if the ad does not specify its own parameters. 

This method will replace any existing custom parameters.

To clear the custom parameters of the keyword, pass an empty object. For example, setCustomParamters({}).  

For more information, see [Custom Parameters](/bingads/guides/url-tracking-upgraded-urls#customparametersvalidation).
### Arguments:
|Name|Type|Description|
|-|-|-
customParameters|Object|The custom parameters of the keyword as a map of the<br />        form <code>{key1: 'value1', key2: 'value2', key3: 'value3'}</code>.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="setfinalurl~string-finalurl~"></a>setFinalUrl(String finalUrl)
Sets the final URL of this keyword.


The final URL represents the actual landing page for your ad. The final URL must be the URL of the page that the user ends up on after clicking on your ad, once all the redirects have taken place.

Final URLs follow the same override rules as destination URLs. For example, a final URL at the keyword level overrides a final URL at an ad level.

### Arguments:
|Name|Type|Description|
|-|-|-
finalUrl|String|The final URL of the keyword.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="settrackingtemplate~string-trackingtemplate~"></a>setTrackingTemplate(String trackingTemplate)
Sets the tracking template of this keyword.


You can optionally use the tracking template to specify additional tracking parameters or redirects. Bing Ads will use this template to assemble the actual destination URL to associate with the ad.

A tracking template specified at a lower level entity will override the setting specified at a higher level entity, for example, a tracking template at the ad group level overrides the setting at the campaign level.
### Arguments:
|Name|Type|Description|
|-|-|-
trackingTemplate|String|The tracking template of the keyword.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

