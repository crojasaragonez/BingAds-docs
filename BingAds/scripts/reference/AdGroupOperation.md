# AdGroupOperation
Represents the definition of an ad group constructed via [AdGroupBuilder](./AdGroupBuilder). The ad group is only stored in the system when any of the methods on this object are invoked or when the script finishes execution, whichever comes first. To make the script execute more efficiently, store the operation objects in an array and only invoke its methods when all operations have been constructed.

# Methods
|Method Name|Return Type|Description|
|-|-|-
[getErrors](#geterrors)|String[]|Returns an empty array if the ad group was successfully created, otherwise returns the errors encountered during the execution of this operation.<br />
[getResult](#getresult)|[AdGroup](./AdGroup)|Returns the newly created ad group, otherwise returns null if this operation failed to execute.<br />
[isSuccessful](#issuccessful)|boolean|Returns a boolean value that determines if the operation was successful.

## <a name="geterrors"></a>getErrors
Returns an empty array if the ad group was successfully created, otherwise returns the errors encountered during the execution of this operation.

### Returns:
|Type|Description|
|-|-
String[]|Errors that occurred during the AdGroupOperation.

## <a name="getresult"></a>getResult
Returns the newly created ad group, otherwise returns null if this operation failed to execute.

### Returns:
|Type|Description|
|-|-
[AdGroup](./AdGroup)|AdGroup created by the AdGroupOperation.

## <a name="issuccessful"></a>isSuccessful
Returns a boolean value that determines if the operation was successful.
### Returns:
|Type|Description|
|-|-
boolean|Boolean value that determines if the operation was successful.

