---
title: Dialog zu Auswahl von Look im Import beim Erstellen einer neuen Timeline in Timeline 3D ausblenden
---

## Dialog zu Auswahl von Look im Import beim Erstellen einer neuen Timeline in Timeline 3D ausblenden

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1, Timeline 3D 2.9.3

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript in Timeline 3D eine neue Timeline erstellen und dabei den Dialog für Look und Import ausblenden.

```applescript
tell application "Timeline 3D"
  activate
  set myTimeline to make new document
    
  tell myTimeline
    set showing panel to false
  end tell
end tell
```
