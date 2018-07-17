## Adresszeile bei WebApps ausblenden

Das folgende Beispiel zeigt, wie man die Adresszeile bei WebApps fürs iPhone beziehungsweise für den iPod touch per JavaScript ausblenden kann:

```javascript
if (window.navigator.standalone == false) {
    window.scrollTo(0, 1);
}
```

### Weiterführende Informationen

- [Safari HTML Reference - Supported Meta Tags (apple-mobile-web-app-capable)](https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html){:target="_blank"}
