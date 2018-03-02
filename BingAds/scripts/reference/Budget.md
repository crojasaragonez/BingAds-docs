# Budget
Represents a budget.
Example usage:
```javascript
 var stats = budget.getStatsFor("THIS_MONTH");
```

# Methods
|Method Name|Return Type|Description|
|-|-|-
[getAmount](#getamount)|double|Returns the amount of this budget, in the currency of the current account.<br />
[getDeliveryMethod](#getdeliverymethod)|String|Returns the delivery method for this budget.
[setAmount(double amount)](#setamount~double-amount~)|void|Sets the amount of this budget to the specified value, in the currency of the current account.<br />
[setDeliveryMethod(String method)](#setdeliverymethod~string-method~)|void|Set the delivery method for this budget.<br />

## <a name="getamount"></a>getAmount
Returns the amount of this budget, in the currency of the current account.

### Returns:
|Type|Description|
|-|-
double|Amount of the budget.
&nbsp;|&nbsp;
## <a name="getdeliverymethod"></a>getDeliveryMethod
Returns the delivery method for this budget. 

Possible return values are:

- STANDARD
- ACCELERATED


### Returns:
|Type|Description|
|-|-
String|Delivery method of the budget.
&nbsp;|&nbsp;
## <a name="setamount~double-amount~"></a>setAmount(double amount)
Sets the amount of this budget to the specified value, in the currency of the current account.

### Arguments:
|Name|Type|Description|
|-|-|-
amount|double|The amount of the budget.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
## <a name="setdeliverymethod~string-method~"></a>setDeliveryMethod(String method)
Set the delivery method for this budget.




### Arguments:
|Name|Type|Description|
|-|-|-
method|String|Sets the delivery method of the budget.<br />
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
void|
&nbsp;|&nbsp;
