---
title: PHP mit AppleScript ausführen
---

## PHP mit AppleScript ausführen

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Wie Sie mit AppleScript ein PHP-Script ausführen, zeigen Ihnen die folgenden Beispiele:

### Beispiel - "Hallo Welt!" ausgeben

```applescript
set myCmd to "php -r \"echo 'Hallo Welt!';\""
set myResult to do shell script myCmd
-- Ergebnis: "Hallo Welt!"
```

### Beispiel - Aktuelle Zeit (Unix-Timestamp) ausgeben

```applescript
set myCmd to "php -r \"echo time();\""
set myResult to do shell script myCmd
-- Ergebnis (zum Beispiel): "1259787423"
```

### Siehe auch

- [URL-Kodierung einer Zeichenkette nach RFC 1738](/mac-os-x/applescript/allgemeines/url-kodierung-einer-zeichenkette-nach-rfc-1738)
