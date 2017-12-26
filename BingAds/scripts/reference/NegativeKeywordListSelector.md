# NegativeKeywordListSelector
Provides methods to select negative keyword lists by using filtering and sorting.

Example usage:
```javascript
while (negativeKeywordListIterator.hasNext()) {
   var negativeKeywordList = negativeKeywordListIterator.next();
 }
```

See also:
- [NegativeKeywordListIterator](./NegativeKeywordListIterator)
- [NegativeKeywordList](./NegativeKeywordList)

# Methods
|Method Name|Return Type|Description|
|-|-|-
[get](#get)|[NegativeKeywordListIterator](./NegativeKeywordListIterator)|Returns an iterator that you use to traverse negative keyword lists.<br />
[orderBy(String orderBy)](#orderby~string-orderby~)|[AdGroupSelector](./AdGroupSelector)|Returns a selector with the specified ordering.
[withCondition(String condition)](#withcondition~string-condition~)|[NegativeKeywordListSelector](./NegativeKeywordListSelector)|Returns a selector with the specified filtering conditions.
[withIds(long[] ids)](#withids~long-ids~)|[NegativeKeywordListSelector](./NegativeKeywordListSelector)|Returns a selector that will return only negative keyword lists with the specified IDs.<br />
[withLimit(int limit)](#withlimit~int-limit~)|[NegativeKeywordListSelector](./NegativeKeywordListSelector)|Returns a selector that will return only the specified number of results from the beginning of the result set.
&nbsp;|&nbsp;|&nbsp;

## <a name="get"></a>get
Returns an iterator that you use to traverse negative keyword lists.

### Returns:
|Type|Description|
|-|-
[NegativeKeywordListIterator](./NegativeKeywordListIterator)|Iterator used to get the negative keywords for this selector.
&nbsp;|&nbsp;
## <a name="orderby~string-orderby~"></a>orderBy(String orderBy)
Returns a selector with the specified ordering.

Specify the orderBy parameter in the form, "columnName orderDirection" where:



- columnName can only be one column which is supported by the withCondition method.

- orderDirection is the direction to order the results in. Set to ASC to order the results in ascending order or DESC to order the results in descending order. The default is ASC.



For example, the following call returns results in ascending order by MaxCpc.

<code>agSelector = agSelector.orderBy("MaxCpc");</code>


Only one orderBy column is supported, specifying more than one will result in an error.

### Arguments:
|Name|Type|Description|
|-|-|-
orderBy|String|Ordering to apply.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[AdGroupSelector](./AdGroupSelector)|The selector with ordering applied.
&nbsp;|&nbsp;
## <a name="withcondition~string-condition~"></a>withCondition(String condition)
Returns a selector with the specified filtering conditions.

Specify the condition parameter in the form, "columnName operator value" where: 

- columnName is the name of a performance metric to order the results by. For a list of possible values, see [Supported Columns](#supported-ad-group-columns).  If you set columName to a performance metric column name, you must also specify a date range using [forDateRange(String dateRange)](#fordaterange~string-daterange~) or [forDateRange(Object dateFrom, Object dateTo)](#fordaterange~object-datefrom_-object-dateto~).
- operator is one of the supported [operators](#operators).

### Operators
The operator that can be used in a condition depends on the type of column. 
For Integer and Long columns: 

```
<  <=  >  >=  =  !=
```
For Double columns: 
```
<  >
```
For String columns: 
```
=  !=  STARTS_WITH  STARTS_WITH_IGNORE_CASE  CONTAINS
 CONTAINS_IGNORE_CASE  DOES_NOT_CONTAIN  DOES_NOT_CONTAIN_IGNORE_CASE
```
For Enumeration columns: 
```
=  !=  IN []  NOT_IN []
```

Operators are case-sensitive: `starts_with` won't work. 

<a name="supported-ad-group-columns"></a>
### Supported Columns

|Column|Type|Example|
|-|-|-|-
<strong>Shared Set Attributes</strong>|
MemberCount|int|`withCondition("MemberCount > 5")`
Name|String|`withCondition("Name = 'negative keyword list'")`
ReferenceCount|int|`withCondition("ReferenceCount > 5")`
SharedSetId|double|`withCondition("SahredSetId > 5")`
Status|Enumeration:<br />&nbsp;`ACTIVE`<br />&nbsp;`DELETED`<br />|`withCondition("Status = ACTIVE")`
&nbsp;|&nbsp;|&nbsp;|&nbsp;


### Arguments:
|Name|Type|Description|
|-|-|-
condition|String|Condition to add to the selector.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[NegativeKeywordListSelector](./NegativeKeywordListSelector)|The selector with the condition applied.
&nbsp;|&nbsp;
## <a name="withids~long-ids~"></a>withIds(long[] ids)
Returns a selector that will return only negative keyword lists with the specified IDs.



The resulting selector can be further filtered by applying additional conditions to it.  All conditions will be 'AND' concatenated including any other ID based conditions.  For example:

```javascript
BingAdsApp.campaigns()
    .withIds([11111, 22222, 33333])
    .withIds([33333, 44444, 55555])
```

will only get the campaign with ID 33333 because it would be the only one satisfying both conditions.

The maximum number of IDs that you may specify is 1,000. If you specify more than 1,000 IDs, calling the get method will fail.

### Arguments:
|Name|Type|Description|
|-|-|-
ids|long[]|Array of ad group IDs.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[NegativeKeywordListSelector](./NegativeKeywordListSelector)|The selector restricted to the given IDs.
&nbsp;|&nbsp;
## <a name="withlimit~int-limit~"></a>withLimit(int limit)
Returns a selector that will return only the specified number of results from the beginning of the result set.
### Arguments:
|Name|Type|Description|
|-|-|-
limit|int|How many entities to return.
&nbsp;|&nbsp;|&nbsp;
### Returns:
|Type|Description|
|-|-
[NegativeKeywordListSelector](./NegativeKeywordListSelector)|The selector with limit applied.
&nbsp;|&nbsp;
