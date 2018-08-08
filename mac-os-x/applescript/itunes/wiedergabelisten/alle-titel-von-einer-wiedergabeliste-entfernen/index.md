---
title: Alle Titel von einer Wiedergabeliste entfernen
---

## Alle Titel von einer Wiedergabeliste entfernen

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1 und iTunes 9.0.2

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript alle Titel von einer Wiedergabeliste entfernen:

```applescript
tell application "iTunes"
  delete every track of playlist "MyPlaylist"
end tell
```

Sie sollten allerding zuvor prüfen, ob es eine Wiedergabeliste mit dem angegebenen Namen gibt. Nur wenn dies der Fall ist, sollen alle Titel von der Wiedergabeliste entfernt werden. Wie Sie dies realisieren, zeigt das folgende Beispiel:

```applescript
tell application "iTunes"
  if exists playlist "MyPlaylist" then
    delete every track of playlist "MyPlaylist"
  end if
end tell
```
