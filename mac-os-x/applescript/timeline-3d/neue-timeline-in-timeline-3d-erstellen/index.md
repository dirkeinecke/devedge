---
title: Neue Timeline in Timeline 3D erstellen
---

## Neue Timeline in Timeline 3D erstellen

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1, Timeline 3D 2.9.3

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript in Timeline 3D eine neue Timeline erstellen.

```applescript
tell application "Timeline 3D"
  activate
  set myTimeline to make new document
end tell
```
