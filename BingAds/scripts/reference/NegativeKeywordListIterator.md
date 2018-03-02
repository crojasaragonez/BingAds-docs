# NegativeKeywordListIterator
Provides methods to iterate through a list of negative keyword lists.

Example usage:
```javascript
while (negativeKeywordListIterator.hasNext()) {
   var negativeKeywordList = negativeKeywordListIterator.next();
 }
```

See also:
- [NegativeKeywordListSelector.get()](./NegativeKeywordListSelector#get)
- [NegativeKeywordList](./NegativeKeywordList)

# Methods
|Method Name|Return Type|Description|
|-|-|-
[hasNext](#hasnext)|boolean|Returns true if the iterator has more negative keyword list elements.
[next](#next)|[AdGroup](./AdGroup)|Advances to the next ad group in this iterator and returns it.<br />
[totalNumEntities](#totalnumentities)|int|Returns the total number of ad groups indexed by this iterator.

## <a name="hasnext"></a>hasNext
Returns true if the iterator has more negative keyword list elements.
### Returns:
|Type|Description|
|-|-
boolean|True if the iterator has more elements.

## <a name="next"></a>next
Advances to the next ad group in this iterator and returns it.

### Returns:
|Type|Description|
|-|-
[AdGroup](./AdGroup)|The next ad group in the iterator.

## <a name="totalnumentities"></a>totalNumEntities
Returns the total number of ad groups indexed by this iterator.


hasNext will start to return false and next will start to throw exceptions when the limit for entity reads has been reached, even if the selector matched more entities.
### Returns:
|Type|Description|
|-|-
int|The number of ad groups matched by the selector which generated this iterator.

