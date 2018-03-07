# AdGroupUrls
Provides access to the URLs for this ad group. See [URL Tracking with Upgraded URLs](/bingads/guides/url-tracking-upgraded-urls) for more information.
Example usage:
```javascript
var adGroupSelector = BingAdsApp.adGroups();

 var adGroupIterator = adGroupSelector.get();
 while (adGroupIterator.hasNext()) {
   var adGroup = adGroupIterator.next();
   var adGroupUrls = adGroup.urls();
   adGroupUrls.getCustomParameters();
 }
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[clearTrackingTemplate](#cleartrackingtemplate)|void|Clears the tracking template of this ad group.<br />
[getCustomParameters](#getcustomparameters)|Object|Returns the custom parameters of this ad group.
[getTrackingTemplate](#gettrackingtemplate)|String|Returns the tracking template of this ad group.<br />
[setCustomParameters(Object customParameters)](#setcustomparameters~object-customparameters~)|void|Sets the custom parameters of this ad group.<br />
[setTrackingTemplate(String trackingTemplate)](#settrackingtemplate~string-trackingtemplate~)|void|Sets the tracking template of this ad group.<br />

## <a name="cleartrackingtemplate"></a>clearTrackingTemplate
Clears the tracking template of this ad group.


[!INCLUDE[tracking-templates](../includes/tracking-templates.md)]

Calling this method removes the tracking template from this ad group. Because tracking templates are inheritable from the parent entity, if the ad group's parent campaign specifies a tracking template, the template also applies to this ad group and its children. If your goal is to not apply the ad group's template to its children (keywords and ads), you must also remove the template from the ad group's parent campaign.

### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="getcustomparameters"></a>getCustomParameters
Returns the custom parameters of this ad group.

An ad group may specify up to three custom parameters. Customer parameter names may contain only alphanumeric characters and must not exceed 16 bytes. When you include custom parameters in final URLs and tracking templates, the convention is to prefix the parameter's name with an underscore and enclose the parameter in curly braces ({}). For example, {_param}.  Custom parameter values may not contain whitespace and must not exceed 200 bytes.

If an ad group does not specify custom parameters, it inherits them from its parent campaign. Likewise, ads in the ad group inherit the parameters from the ad group if the ad does not specify its own parameters. 

For more information, see [Custom Parameters](/bingads/guides/url-tracking-upgraded-urls#customparametersvalidation).
### Returns:
|Type|Description|
|-|-
Object|The custom parameters of the ad group as a map of the form: `{key1: 'value1', key2: 'value2', key3: 'value3'}`.

## <a name="gettrackingtemplate"></a>getTrackingTemplate
Returns the tracking template of this ad group.


[!INCLUDE[tracking-templates](../includes/tracking-templates.md)]
### Returns:
|Type|Description|
|-|-
String|The tracking template of the ad group.

## <a name="setcustomparameters~object-customparameters~"></a>setCustomParameters(Object customParameters)
Sets the custom parameters of this ad group.


An ad group may specify up to three custom parameters. Customer parameter names may contain only alphanumeric characters and must not exceed 16 bytes. When you include custom parameters in final URLs and tracking templates, the convention is to prefix the parameter's name with an underscore and enclose the parameter in curly braces ({}). For example, {_param}.  Custom parameter values may not contain whitespace and must not exceed 200 bytes.

If an ad group does not specify custom parameters, it inherits them from its parent campaign. Likewise, ads in the ad group inherit the parameters from the ad group if the ad does not specify its own parameters. 

For more information, see [Custom Parameters](/bingads/guides/url-tracking-upgraded-urls#customparametersvalidation).

This method replaces any existing custom parameters.

To clear the custom parameters of the ad group pass an empty object, for example `setCustomParameters({})`.  
### Arguments:
|Name|Type|Description|
|-|-|-
customParameters|Object|The custom parameters of the ad group as a map of the<br />        form <code>{key1: 'value1', key2: 'value2', key3: 'value3'}</code>.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="settrackingtemplate~string-trackingtemplate~"></a>setTrackingTemplate(String trackingTemplate)
Sets the tracking template of this ad group.


[!INCLUDE[tracking-templates](../includes/tracking-templates.md)]
### Arguments:
|Name|Type|Description|
|-|-|-
trackingTemplate|String|The tracking template of the ad group.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

