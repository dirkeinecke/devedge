---
title: Vorderstes Dokument (Timeline) in Timeline 3D referenzieren
---

## Vorderstes Dokument (Timeline) in Timeline 3D referenzieren

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1, Timeline 3D 2.9.3

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript in Timeline 3D das vorderste Dokument (Timeline) referenzieren.

```applescript
tell application "Timeline 3D"
  activate
  set myTimeline to front document
end tell
```
