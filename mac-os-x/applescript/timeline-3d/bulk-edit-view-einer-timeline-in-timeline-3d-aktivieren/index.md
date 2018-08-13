---
title: Listenansicht (Bulk Edit View) einer Timeline in Timeline 3D aktivieren
---

## Listenansicht (Bulk Edit View) einer Timeline in Timeline 3D aktivieren

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1, Timeline 3D 2.9.3

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript in Timeline 3D den Ansicht-Typ auf "Listenansicht" (Bulk Edit View) ändern.

### Beispiel #1 - anhand eines neuen Dokuments (Zeitstrahls)

```applescript
tell application "Timeline 3D"
  activate
  set myTimeline to make new document
    
  tell myTimeline
    set view mode to bulk edit view
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
  end tell
end tell
```

### Siehe auch

- [Bildschirmansicht (Screen View) einer Timeline in Timeline 3D aktivieren](/mac-os-x/applescript/timeline-3d/screen-view-einer-timeline-in-timeline-3d-aktivieren){:target="_blank"}
