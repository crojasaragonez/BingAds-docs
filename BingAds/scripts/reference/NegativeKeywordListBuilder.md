# NegativeKeywordListBuilder
Provides methods for defining and building a negative keyword list.

Example usage:
```javascript
 var negativeKeywordListBuilder = BingAdsApp.newNegativeKeywordListBuilder()
         .withName("NegativeKeywordList");

 var negativeKeywordListOperation = negativeKeywordListBuilder.build();

 var negativeKeywordList = negativeKeywordListOperation.getResult();
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[build](#build)|[NegativeKeywordListOperation](./NegativeKeywordListOperation)|Returns an operation object with the defined properties which can later be used to construct the keyword.<br />
[withName(String name)](#withname~string-name~)|[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|Returns a negative keyword list builder with the name set to the specified value.<br />

## <a name="build"></a>build
Returns an operation object with the defined properties which can later be used to construct the keyword.

### Returns:
|Type|Description|
|-|-
[NegativeKeywordListOperation](./NegativeKeywordListOperation)|Operation object with the defined properties which can later be used to construct the keyword.

## <a name="withname~string-name~"></a>withName(String name)
Returns a negative keyword list builder with the name set to the specified value.

### Arguments:
|Name|Type|Description|
|-|-|-
name|String|The name of the new negative keyword list.
### Returns:
|Type|Description|
|-|-
[NegativeKeywordListBuilder](./NegativeKeywordListBuilder)|Negative keyword list builder with the name set to the specified value.

