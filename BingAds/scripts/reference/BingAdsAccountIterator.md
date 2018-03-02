# BingAdsAccountIterator
Provides methods to iterate through Bing Ads accounts.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[hasNext](#hasnext)|boolean|Returns true if this iterator has more Bing Ads account elements. <br />
[next](#next)|[BingAdsAccount](./BingAdsAccount)|Advances to the next Bing Ads account in this iterator and returns it.<br />
[totalNumEntities](#totalnumentities)|int|Returns the total number of bing ads accounts indexed by this iterator.

## <a name="hasnext"></a>hasNext
Returns true if this iterator has more Bing Ads account elements. 

### Returns:
|Type|Description|
|-|-
boolean|True if this iterator has more Bing Ads account elements.
&nbsp;|&nbsp;
## <a name="next"></a>next
Advances to the next Bing Ads account in this iterator and returns it.

### Returns:
|Type|Description|
|-|-
[BingAdsAccount](./BingAdsAccount)|The next bing ads account in the iterator.
&nbsp;|&nbsp;
## <a name="totalnumentities"></a>totalNumEntities
Returns the total number of bing ads accounts indexed by this iterator.

hasNext will start to return false and next will start to throw exceptions when the limit for entity reads has been reached, even if the selector matched more entities.

### Returns:
|Type|Description|
|-|-
int|The number of bing ads accounts matched by the selector which generated this iterator.
&nbsp;|&nbsp;
