# CampaignUrls
Provides access to the URLs for this campaign.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[clearTrackingTemplate](#cleartrackingtemplate)|void|Clears the tracking template of this campaign.<br />
[getCustomParameters](#getcustomparameters)|Object|Returns the custom parameters of this campaign.
[getTrackingTemplate](#gettrackingtemplate)|String|Returns the tracking template of this campaign.<br />
[setCustomParameters(Object customParameters)](#setcustomparameters~object-customparameters~)|void|Sets the custom parameters of this campaign.<br />
[setTrackingTemplate(String trackingTemplate)](#settrackingtemplate~string-trackingtemplate~)|void|Sets the tracking template of this campaign.<br />

## <a name="cleartrackingtemplate"></a>clearTrackingTemplate
Clears the tracking template of this campaign.


For more information, see [Tracking Templates](/bingads/guides/url-tracking-upgraded-urls#trackingtemplatevalidation).
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="getcustomparameters"></a>getCustomParameters
Returns the custom parameters of this campaign. 

An ad group may specify up to three custom parameters. Customer parameter names may contain only alphanumeric characters and must not exceed 16 bytes. When you include custom parameters in final URLs and tracking templates, the convention is to prefix the parameter's name with an underscore and enclose the parameter in curly braces ({}). For example, {_param}.  Custom parameter values may not contain whitespace and must not exceed 200 bytes.

If an ad group does not specify custom parameters, it inherits them from its parent campaign. Likewise, ads in the ad group inherit the parameters from the ad group if the ad does not specify its own parameters. 

For more information, see [Custom Parameters](/bingads/guides/url-tracking-upgraded-urls#customparametersvalidation).
### Returns:
|Type|Description|
|-|-
Object|The custom parameters of the campaign as a map of the following form: `{key1: 'value1', key2: 'value2', key3: 'value3'}`.

## <a name="gettrackingtemplate"></a>getTrackingTemplate
Returns the tracking template of this campaign.


[!INCLUDE[tracking-templates](../includes/tracking-templates.md)]
### Returns:
|Type|Description|
|-|-
String|The tracking template of the campaign.

## <a name="setcustomparameters~object-customparameters~"></a>setCustomParameters(Object customParameters)
Sets the custom parameters of this campaign.


An ad group may specify up to three custom parameters. Customer parameter names may contain only alphanumeric characters and must not exceed 16 bytes. When you include custom parameters in final URLs and tracking templates, the convention is to prefix the parameter's name with an underscore and enclose the parameter in curly braces ({}). For example, {_param}.  Custom parameter values may not contain whitespace and must not exceed 200 bytes.

If an ad group does not specify custom parameters, it inherits them from its parent campaign. Likewise, ads in the ad group inherit the parameters from the ad group if the ad does not specify its own parameters. 

For more information, see [Custom Parameters](/bingads/guides/url-tracking-upgraded-urls#customparametersvalidation).

This method will replace any existing custom parameters.

To clear the custom parameters of the campaign pass an empty object, for example `setCustomParamters({})`.  If custom parameters are cleared at a lower level entity (for example a keyword). and custom parameters are specified on a higher level entity, (for example, the parent ad group), then Bing Ads uses the custom parameters specified at the higher level (for example, the ad group custom parameters will be used).  To completely clear custom parameters they must be cleared at all levels.
### Arguments:
|Name|Type|Description|
|-|-|-
customParameters|Object|The custom parameters of the campaign as a map of the<br /> form <code>{key1: 'value1', key2: 'value2', key3: 'value3'}</code>.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="settrackingtemplate~string-trackingtemplate~"></a>setTrackingTemplate(String trackingTemplate)
Sets the tracking template of this campaign.


[!INCLUDE[tracking-templates](../includes/tracking-templates.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
trackingTemplate|String|The tracking template of the campaign.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

