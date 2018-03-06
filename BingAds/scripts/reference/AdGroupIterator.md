# AdGroupIterator
Provides methods to iterate through a list of ad groups.

Example usage:
```javascript
 while (adGroupIterator.hasNext()) {
   var adGroup = adGroupIterator.next();
 }
```

See also:
- [AdGroupSelector.get()](./AdGroupSelector#get)
- [AdGroup](./AdGroup)

# Methods
|Method Name|Return Type|Description|
|-|-|-
[hasNext](#hasnext)|boolean|Returns true if the iterator has more ad group elements.
[next](#next)|[AdGroup](./AdGroup)|Advances to the next ad group in this iterator and returns it.<br />
[totalNumEntities](#totalnumentities)|int|Returns the total number of ad groups indexed by the iterator.

## <a name="hasnext"></a>hasNext
Returns true if the iterator has more ad group elements.
### Returns:
|Type|Description|
|-|-
boolean|A boolean value that determines if the iterator has more elements.

## <a name="next"></a>next
Advances to the next ad group in this iterator and returns it.

### Returns:
|Type|Description|
|-|-
[AdGroup](./AdGroup)|The next ad group in the iterator.

## <a name="totalnumentities"></a>totalNumEntities
Returns the total number of ad groups indexed by the iterator.


### Returns:
|Type|Description|
|-|-
int|The number of ad groups matched by the selector that generated the iterator.

