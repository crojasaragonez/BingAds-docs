# AdGroup
Represents an ad group in the Bing Ads system.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[enable](#enable)|void|Enables this ad group.<br />
[getEntityType](#getentitytype)|String|Returns the entity type of this ad group, which is "AdGroup".<br />
[getId](#getid)|long|Returns the ID of the ad group.<br />
[getName](#getname)|String|Returns the name of this ad group.<br />
[isEnabled](#isenabled)|boolean|Returns true if this ad group is enabled. <br />
[isPaused](#ispaused)|boolean|Returns true if this ad group is paused. <br />
[pause](#pause)|void|Pauses this ad group.<br />
[setName(String name)](#setname~string-name~)|void|Sets the name of this ad group.<br />
[urls](#urls)|[AdGroupUrls](./AdGroupUrls)|Returns an AdGroupUrls object which provides access to the URL fields of this ad group.<br />
[newKeywordBuilder](#newkeywordbuilder)|[KeywordBuilder](./KeywordBuilder)|Returns a new keyword builder associated with this ad group that is used to construct a new keyword.<br />

## <a name="enable"></a>enable
Enables this ad group.

### Returns:
|Type|Description|
|-|-
void|Returns nothing

## <a name="getentitytype"></a>getEntityType
Returns the entity type of this ad group, which is "AdGroup".

### Returns:
|Type|Description|
|-|-
String|Type of this entity.

## <a name="getid"></a>getId
Returns the ID of the ad group.

### Returns:
|Type|Description|
|-|-
long|The ID of the ad group.

## <a name="getname"></a>getName
Returns the name of this ad group.

### Returns:
|Type|Description|
|-|-
String|The name of the ad group.

## <a name="isenabled"></a>isEnabled
Returns true if this ad group is enabled. 

### Returns:
|Type|Description|
|-|-
boolean|A boolean value that determines whether the ad group is enabled.

## <a name="ispaused"></a>isPaused
Returns true if this ad group is paused. 

### Returns:
|Type|Description|
|-|-
boolean|true if the ad group is paused.

## <a name="pause"></a>pause
Pauses this ad group.

### Returns:
|Type|Description|
|-|-
void|Returns nothing

## <a name="setname~string-name~"></a>setName(String name)
Sets the name of this ad group.

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The name for the ad group.
### Returns:
|Type|Description|
|-|-
void|Returns nothing.

## <a name="urls"></a>urls
Returns an AdGroupUrls object which provides access to the URL fields of this ad group.

### Returns:
|Type|Description|
|-|-
[AdGroupUrls](./AdGroupUrls)|an AdGroupUrls object which provides access to the URL fields of this ad group.

## <a name="newkeywordbuilder"></a>newKeywordBuilder
Returns a new keyword builder associated with this ad group that is used to construct a new keyword.

### Returns:
|Type|Description|
|-|-
[KeywordBuilder](./KeywordBuilder)|A new keyword builder associated with this ad group that is used to construct a new keyword.

