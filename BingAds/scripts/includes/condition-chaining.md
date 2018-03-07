You may apply one or more conditions to a selector. A chain of conditions is considered an AND operation. If condition A is true AND condition B is true, select the entity. For example, the following call selects only ad group 33333.

```javascript
BingAdsApp.adGroups()
    .withIds([11111, 22222, 33333])
    .withIds([33333, 44444, 55555])
```
