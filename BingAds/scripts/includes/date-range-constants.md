Supported date range values:

- TODAY
- YESTERDAY
- LAST_7_DAYS
- THIS_WEEK_SUN_TODAY
- LAST_14_DAYS
- LAST_30_DAYS
- LAST_WEEK_SUN_SAT
- THIS_MONTH
- LAST_MONTH
- ALL_TIME

Example:
```javascript
selector.forDateRange("LAST_7_DAYS");
```

If you apply conditions or ordering that reference performance metric fields, you must specify a date range.  Only the last date range specified will be used.
