---
title: Datei verschieben
---

## Datei verschieben

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man eine Datei verschieben möchte, dann kann man dies wie folgt tun:

```applescript
set theFile to (path to desktop) & "datei.rtf" as text
set theNewFolder to (path to documents folder)
tell application "Finder"
  move file theFile to theNewFolder
end tell
```
