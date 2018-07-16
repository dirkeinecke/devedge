## Benutzerdefinierte Fehlerseiten

Möchte man selbst definieren, welche Dateien bei bestimmten Fehlern angezeigt werden,
dann kann man dies über eine .htaccess-Datei erledigen. Man braucht dazu nur die folgenden
Zeilen in die .htaccess-Datei einfügen - und die Pfade zu den Dateien die angezeigt werden
sollen natürlich noch anpassen.

```apache_conf
ErrorDocument 401 /Fehlerseiten/401.html
ErrorDocument 403 /Fehlerseiten/403.html
ErrorDocument 404 /Fehlerseiten/404.html
ErrorDocument 500 /Fehlerseiten/500.html
```

### Weiterführende Informationen

- [Apache HTTP Server - ErrorDocument-Direktive](https://httpd.apache.org/docs/2.0/mod/core.html#errordocument){:target="_blank"}
