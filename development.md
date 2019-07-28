


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

## fanout
- https://getstream.io/
- https://fanout.io/
- https://www.quora.com/Activity-Streams/What-are-the-scaling-issues-to-keep-in-mind-while-developing-a-social-network-feed
- https://stackoverflow.com/questions/1443960/how-to-implement-the-activity-stream-in-a-social-network
