# Get Started With Bing Ads Scripts

> [!NOTE]
> This preview release of Bing Ads Scripts is available to select participants only. For information about participating in the preview release program, please contact your account manager.
>
> The Scripts API, and documentation are subject to change.

1. Sign in to [Bing Ads](https://secure.bingads.microsoft.com/).
2. Expand <strong>Bulk Operations</strong> (see the left navigation panel).
3. Click <strong>Scripts</strong>.
4. Copy and paste the following code into the code editor.
```javascript
function main() {
    var keywords = BingAdsApp.keywords()
        .orderBy("Impressions DESC")
        .forDateRange("YESTERDAY")
        .withLimit(10)
        .get();

    Logger.log("10 keywords with most impressions yesterday");
    while (keywords.hasNext()) {
        var keyword = keywords.next();
        Logger.log(keyword.getText() + ": " +
            keyword.getStatsFor("YESTERDAY").getImpressions());
    }
}
main();
```
5. To execute the script in preview mode, click <strong>Preview</strong>.