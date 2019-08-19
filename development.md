


## Service workers
- [is service worker ready? Yes!](https://jakearchibald.github.io/isserviceworkerready/resources.html)
- [Service Workers: an introduction](https://developers.google.com/web/fundamentals/primers/service-workers/?hl=en)
- [A beginner’s guide to Service Workers](https://medium.com/samsung-internet-dev/a-beginners-guide-to-service-workers-f76abf1960f6)
- PWA
  - [Introduction to Service Worker](https://developers.google.com/web/ilt/pwa/introduction-to-service-worker)
  - [Introduction to Push Notifications](https://developers.google.com/web/ilt/pwa/introduction-to-push-notifications)
- :tv: [Alexander Pope: ServiceWorkers Outbreak: index-sw-9a4c43b4b47781ca619eaaf5ac1db.js](https://www.youtube.com/watch?v=CPP9ew4Co0M)
- :tv: [The Service Worker Lifecycle](https://www.youtube.com/watch?v=TF4AB75PyIc)
- [Debugging Service Workers](https://developers.google.com/web/fundamentals/codelabs/debugging-service-workers/?hl=en)
- [Cookbook](https://serviceworke.rs/api-analytics_service-worker_doc.html)
- https://developers.google.com/web/tools/workbox/guides/get-started
- https://www.simicart.com/blog/pwa-ios-13-beta/

## Push Notifications
- [Web Push Notifications: Timely, Relevant, and Precise](https://developers.google.com/web/fundamentals/push-notifications/)
- :tv: [Push Notifications Using Node.js & Service Worker](https://www.youtube.com/watch?v=HlYFW2zaYQM)
- :tv: [Web Push Notifications in Xampp with PHP](https://www.youtube.com/watch?v=vi9d6MjiBGQ)
- [Sending Web Push Notifications from Node.js](https://thecodebarbarian.com/sending-web-push-notifications-from-node-js.html)
- https://www.simicart.com/blog/pwa-ios-13-beta/

## tracking and analytics
- https://www.simoahava.com/analytics/measure-serp-bounce-time-with-gtm/
- https://github.com/Countly/countly-sdk-web
- https://www.analyticsmania.com/post/custom-javascripts-for-google-tag-manager/
- https://developers.google.com/analytics/resources/concepts/gaConceptsTrackingOverview
- [Sending Data to Server on Page Unload](http://qnimate.com/sending-data-to-server-on-page-unload/) o http://usefulangle.com/post/62/javascript-send-data-to-server-on-page-exit-reload-redirect
- https://github.com/twail-net/visibilityjs

```
window.addEventListener('unload', logData, false);

function logData() {
    if("sendBeacon" in navigator)
    {
        navigator.sendBeacon("/log", analyticsData);
    }
    else
    {
        var client = new XMLHttpRequest();
        client.open("POST", "/log", false);
        client.send(analyticsData);
    }
}
```

- Alternativas a Google Analytics
  - Matomo, antes piwik (https://matomo.org/)
  - http://www.openwebanalytics.com/
  - https://count.ly/web-analytics
  - https://keen.io/ (https://github.com/keen/keen-tracking.js/)
  - http://www.eventanalytics.org/
  - https://github.com/snowplow/snowplow-javascript-tracker

- Parametros que envía Google analytics

Google envía hace una para enviar los datos recurrentemente...

```
https://www.google-analytics.com/collect?v=1&_v=j68&a=753537405&t=pageview&_s=1&dl=https%3A%2F%2Fwww.analyticsmarket.com%2F&ul=en-us&de=UTF-8&dt=Resources%20for%20Google%20Analytics&sd=24-bit&sr=1600x900&vp=1583x418&je=0&_u=AACAAEAB~&jid=1528408694&gjid=192180985&cid=1602946763.1549335544&tid=UA-23423231144-1&_gid=1845815927.1549335544&_r=1&z=549945300
```

Name|Description|Example Value
|---|---|---|
v|Protocol version|v=1
_v|SDK Version number|_v=j68
a|AdSense linking number|a=753537405
t|Hit Type.  e.g. pageview, event, item, timing, etc.|t=pageview
_s|Hit sequence number? (unsure)|_s=1
dl|Document Location (full URL)|dl=https%3A%2F%2Fwww.analyticsmarket.com%2F
ul|User Language|ul=en-us
de|Document Encoding|de=UTF-8
dt|Document Title (Page Title)|dt=Resources%20for%20Google%20Analytics
sd|Screen Depth (color)|sd=24-bit
sr|Screen Resolution|sr=1600×900
vp|View Port|vp=1583×418
je|Java Enabled (0 = no, 1 = yes)|je=0
_u|Usage info: tells Google which features are used|_u=AACAAEAB~
jid|Join ID for DoubleClick beacon|jid=1528408694
gjid|Tracking code version|gjid=192180985
cid|Client ID: random-number.timestamp|cid=1602946763.1549335544
tid|Tracking ID / Web Property ID|tid=UA-23423231144-1
_gid|User ID, used to distinguish users|_gid=1845815927.1549335544
z|Random Number Cache Buster|z=549945300




## fanout
- https://getstream.io/
- https://fanout.io/
- https://www.quora.com/Activity-Streams/What-are-the-scaling-issues-to-keep-in-mind-while-developing-a-social-network-feed
- https://stackoverflow.com/questions/1443960/how-to-implement-the-activity-stream-in-a-social-network
