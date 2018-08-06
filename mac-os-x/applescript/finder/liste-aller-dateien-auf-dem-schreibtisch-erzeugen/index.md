---
title: Liste aller Dateien auf dem Schreibtisch erzeugen
---

## Liste aller Dateien auf dem Schreibtisch erzeugen

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Wie Sie eine Liste aller Dokumente auf dem Schreibtisch (`desktop`) erzeugen können, zeigt Ihnen das folgende Script:

```applescript
tell application "Finder"
  files of desktop as alias list
end tell
```
