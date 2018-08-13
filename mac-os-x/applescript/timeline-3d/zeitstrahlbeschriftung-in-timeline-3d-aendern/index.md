---
title: Zeitstrahlbeschriftung in Timeline 3D ändern
---

## Zeitstrahlbeschriftung in Timeline 3D ändern

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1, Timeline 3D 2.9.3

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript in Timeline 3D die Zeitrahlbeschriftung ändern (hier in "`Mein Zeitstrahl`").

### Beispiel #1 - anhand eines neuen Dokuments (Zeitstrahls)

```applescript
tell application "Timeline 3D"
  activate
  set myTimeline to make new document
    
  tell myTimeline
    set view mode to bulk edit view
    set name of first row to "Mein Zeitstrahl"
  end tell
end tell
```

### Beispiel #2 - anhand eines vorhandenen Dokuments (Zeitstrahls)

```applescript
tell application "Timeline 3D"
  activate
  set myTimeline to front document
    
  tell myTimeline
    set view mode to bulk edit view
    set name of first row to "Mein Zeitstrahl"
  end tell
end tell
```
