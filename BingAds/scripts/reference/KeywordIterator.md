# KeywordIterator
Provides methods to iterate through keywords.

Example usage:
```javascript
 while (keywordIterator.hasNext()) {
   var keyword = keywordIterator.next();
 }
```

See also:

- [KeywordSelector.get()](./KeywordSelector#get)
- [Keyword](./Keyword)


# Methods
|Method Name|Return Type|Description|
|-|-|-
[hasNext](#hasnext)|boolean|Returns true if this iterator has more keyword elements.<br />
[next](#next)|[Keyword](./Keyword)|Advances to the next keyword in this iterator and returns it.<br />
[totalNumEntities](#totalnumentities)|int|Returns the total number of keywords indexed by this iterator.

## <a name="hasnext"></a>hasNext
Returns true if this iterator has more keyword elements.

### Returns:
|Type|Description|
|-|-
boolean|Boolean value that determines if this iterator has more keyword elements.

## <a name="next"></a>next
Advances to the next keyword in this iterator and returns it.

### Returns:
|Type|Description|
|-|-
[Keyword](./Keyword)|Next keyword in the iterator.

## <a name="totalnumentities"></a>totalNumEntities
Returns the total number of keywords indexed by this iterator.

hasNext will start to return false and next will start to throw exceptions when the limit for entity reads has been reached, even if the selector matched more entities.
### Returns:
|Type|Description|
|-|-
int|Number of keywords matched by the selector which generated this iterator.

