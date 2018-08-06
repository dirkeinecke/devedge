---
title: Informationsfenster einer Datei oder eines Ordners anzeigen
---

## Informationsfenster einer Datei oder eines Ordners anzeigen

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript das Informationsfenster einer Datei bzw. eines Ordners anzeigen:

```applescript
-- Datei auswählen
set myItem to choose file without invisibles

tell application "Finder"
  activate
  -- Informationsfenster anzeigen
  open the information window of item myItem
end tell
```
