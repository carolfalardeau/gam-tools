# Google Ad Manager - Tools
## Ads logging - Bookmark
Show ads logs in Console.
- Add a new bookmark in you browser
- Add this code in the url: 
```
javascript:console.log(" _____   ______  _____      _               \n|  __ \\ |  ____||  __ \\    | |              \n| |  | || |__   | |__) |   | |  ___    __ _ \n| |  | ||  __|  |  ___/    | | / _ \\  / _` |\n| |__| || |     | |        | || (_) || (_| |\n|_____/ |_|     |_|        |_| \\___/  \\__, |\n                                       __/ |\n                                      |___/ \n\n");var adTargetingKeys=googletag.pubads().getTargetingKeys();adTargetingKeys.forEach(function(o,e){0==e&&console.group("Page targeting ("+adTargetingKeys.length+")");var n=googletag.pubads().getTargeting(o);console.log(o+": "+n.join(", ")),e==adTargetingKeys.length-1&&console.groupEnd()}),console.log("");var adSlots=googletag.pubads().getSlots();console.group("Ads slots ("+adSlots.length+")"),adSlots.forEach(function(o,e){console.group(o.getSlotElementId()+" ("+(e+1)+")"),console.log("Element ID: "+o.getSlotElementId()),console.log("Unit path: "+o.getSlotId().getAdUnitPath());var n=o.getSizes(),g="";if(n.forEach(function(o,e){void 0!==o.getWidth?g+=o.getWidth()+"x"+o.getHeight():g+=o,e==n.length-1?console.log("Ad size: "+g):g+=", "}),console.log(""),void 0!==o.ka&&null!==o.ka&&void 0!==o.ka.j){console.group("Ad sizes");for(var l=o.ka.j,t=0;t<l.length;t++){var _=l[t].l.width+"x"+l[t].l.height+": ",s=[];for(j=0;j<l[t].j.length;j++)s.push(l[t].j[j].getWidth()+"x"+l[t].j[j].getHeight());_+=s.join(", "),console.log(_)}console.groupEnd(),console.log("")}var a=o.getTargetingMap();Object.keys(a).length>0&&(Object.keys(a).map(function(o,e){0==e&&console.group("Slot targeting ("+a[o].length+")"),console.log(o+": "+a[o].join(", ")),e==Object.keys(a).length-1&&console.groupEnd()}),console.log(""));var c=o.getResponseInformation();c?(console.groupCollapsed("Creative info"),console.log("Advertiser ID: "+c.advertiserId),console.log("Campaign ID: "+c.campaignId),console.log("Creative ID: "+c.creativeId),console.log("Line Item ID: "+c.lineItemId),console.groupEnd()):console.log("Empty creative"),console.groupEnd(),e<adSlots.length-1&&console.log("")}),console.groupEnd();
```
- Open the devtools
- Click on the bookmark
## Open GAM Console - Bookmark
Open the Google Ad Manager (GAM) Console on the website
- Add a new bookmark in you browser
- Add this code in the url: 
``
javascript:googletag.openConsole();
``
- Click on the bookmark
## Show targeting keys - Bookmark
Show page targeting keys/values in an alert.
- Add a new bookmark in you browser
- Add this code in the url: 
```
javascript:var adTargetingKeys = googletag.pubads().getTargetingKeys(); var adTargetingList = []; adTargetingKeys.forEach(function(adTargetingKey, indexAdTargetingKey) { var adTargetingValues = googletag.pubads().getTargeting(adTargetingKey); adTargetingList.push(adTargetingKey + ': ' + adTargetingValues.join(', ')); }); alert(adTargetingList.join('\n'));
```
- Click on the bookmark
