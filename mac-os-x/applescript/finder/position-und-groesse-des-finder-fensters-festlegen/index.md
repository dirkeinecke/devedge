---
title: Position und Größe des Finder-Fensters festlegen
---

## Position und Größe des Finder-Fensters festlegen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Position und Größe des Finder-Fensters festlegen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  activate
  select Finder window 1
  set bounds of Finder window 1 to {100, 100, 900, 700} -- links, oben, Breite, Höhe
end tell
```
