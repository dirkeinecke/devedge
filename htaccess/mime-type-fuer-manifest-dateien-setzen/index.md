## MIME-Type für manifest-Dateien setzen

Wenn man zum Beispiel WebApps für das iPhone oder den iPod touch als Offline-Anwendung erstellen möchte,
dann muss man dazu eine .manifest-Datei erstellen. Damit diese auch mit dem text/cache-manifest MIME-Type
vom Webserver ausgeliefert werden, muss man in eine .htaccess-Datei folgenden Eintrag machen:

```
AddType text/cache-manifest .manifest
```

### Weiterführende Informationen

- [HTML 5 Offline Application Cache](https://developer.apple.com/library/archive/documentation/iPhone/Conceptual/SafariJSDatabaseGuide/OfflineApplicationCache/OfflineApplicationCache.html){:target="_blank"}
