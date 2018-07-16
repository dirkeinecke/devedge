## Alle Verzeichnisse und Dateien von einer Domain auf eine andere Domain umleiten

Möchte man alle Verzeichnisse und Dateien von Domain A nach Domain B umleiten, dann muss man dazu auf Domain A eine .htaccess-Datei mit folgendem Inhalt anlegen:

```apache_conf
RedirectPermanent / http://www.domain-b.de/
```

Somit werden dann alle Aufrufe von zum Beispiel `http://www.domain-a.de/ordner-1/datei-2.html` nach `http://www.domain-b.de/ordner-1/datei-2.html` umgeleitet.
