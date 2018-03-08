# NegativeKeywordListOperation
Represents the definition of a keyword constructed via [NegativeKeywordListBuilder](./NegativeKeywordListBuilder). The negative keyword list is only stored in the system when any of the methods on this object are invoked or when the script finishes execution, whichever comes first. To make the script execute more efficiently, store the operation objects in an array and only invoke its methods when all operations have been constructed.
# Methods
|Method Name|Return Type|Description|
|-|-|-
[getErrors](#geterrors)|String[]|Returns an empty array if the keyword was successfully created, otherwise returns the errors encountered during the execution of this operation.<br />
[getResult](#getresult)|[NegativeKeywordList](./NegativeKeywordList)|Returns the newly created NegativeKeywordList, otherwise returns null if the operation failed.<br />
[isSuccessful](#issuccessful)|boolean|Returns a boolean value that determines if the operation was successful.

## <a name="geterrors"></a>getErrors
Returns an empty array if the keyword was successfully created, otherwise returns the errors encountered during the execution of this operation.

### Returns:
|Type|Description|
|-|-
String[]|Errors that occurred during the operation.

## <a name="getresult"></a>getResult
Returns the newly created NegativeKeywordList, otherwise returns null if the operation failed.

### Returns:
|Type|Description|
|-|-
[NegativeKeywordList](./NegativeKeywordList)|NegativeKeywordList created by the NegativeKeywordListOperation.

## <a name="issuccessful"></a>isSuccessful
Returns a boolean value that determines if the operation was successful.
### Returns:
|Type|Description|
|-|-
boolean|Boolean value that determines if the operation was successful.

