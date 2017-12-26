# NegativeKeywordListBuilder
Provides methods for defining and building a negative keyword list.

Example usage:
```javascript
 var negativeKeywordListOperation =
     BingAdsApp.newNegativeKeywordListBuilder()
         .withName("NegativeKeywordList")
         .build();
 var negativeKeywordList = negativeKeywordListOperation.getResult();
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[build](#build)|[NegativeKeywordListOperation](./NegativeKeywordListOperation)|Returns an operation object with the defined properties which can later be used to construct the keyword.<br />
[withName(String name)](#withname~string-name~)|[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|Returns a negative keyword list builder with the name set to the specified value.<br />
&nbsp;|&nbsp;|&nbsp;

## <a name="build"></a>build
Returns an operation object with the defined properties which can later be used to construct the keyword.

### Returns:
|Type|Description|
|-|-
[NegativeKeywordListOperation](./NegativeKeywordListOperation)|An operation object with the defined properties which can later be used to construct the keyword.
&nbsp;|&nbsp;
## <a name="withname~string-name~"></a>withName(String name)
Returns a negative keyword list builder with the name set to the specified value.

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The name of the new negative keyword list.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|A negative keyword list builder with the name set to the specified value.
&nbsp;|&nbsp;
