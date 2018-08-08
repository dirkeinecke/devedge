---
title: Neue Wiedergabeliste erstellen
---

## Neue Wiedergabeliste erstellen

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1 und iTunes 9.0.2

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript eine neue Wiedergabeliste in iTunes erstellen:

```applescript
tell application "iTunes"
  make new playlist at beginning with properties {name:"MyNewPlaylist"}
end tell
```

Sie sollten allerding zuvor prüfen, ob es bereits eine Wiedergabeliste mit dem gewählten Namen gibt. Nur wenn dies nicht der Fall ist, soll die neue Wiedergabeliste mit dem gewählten Namen erstellt werden. Wie Sie dies realisieren, zeigt das folgende Beispiel:

```applescript
tell application "iTunes"
  if not (exists playlist "MyNewPlaylist") then
    make new playlist at beginning with properties {name:"MyNewPlaylist"}
  end if
end tell
```
