---
title: Prüfen ob eine Wiedergabeliste mit einen bestimmten Namen existiert
---

## Prüfen ob eine Wiedergabeliste mit einen bestimmten Namen existiert

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1 und iTunes 9.0.2

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript überprüfen können, ob eine Wiedergabeliste mit einem bestimmten Namen existiert:

```applescript
tell application "iTunes"
  if exists playlist "MyPlaylist" then
    display dialog "Es gibt eine Wiedergabeliste mit dem Namen 'MyPlaylist'."
  end if
end tell
```
