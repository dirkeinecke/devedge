---
title: Pfad zum aktuellen Programm ermitteln
---

## Pfad zum aktuellen Programm ermitteln

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript den Pfad zum aktuellen Programm (über welches das AppleScript ausgeführt wird) ermitteln:

```applescript
tell application "Finder"
  set myPath to path to me
end tell

-- Ergebnis: alias "Macintosh HD:Applications:Utilities:AppleScript Editor.app:"
```
