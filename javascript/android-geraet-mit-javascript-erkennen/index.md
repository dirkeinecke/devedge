## Android-Gerät mit JavaScript erkennen

Das folgende Beispiel zeigt, wie man von ein Android-Gerät mit JavaScript erkennen kann.

```javascript
var ua = navigator.userAgent.toLowerCase();
var isAndroid = ua.indexOf('android') > -1;

if (isAndroid) {
  alert('Hallo Android.');
}
```
