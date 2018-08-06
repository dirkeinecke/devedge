---
title: Pfad zum Ordner des aktuellen Programms ermitteln
---

## Pfad zum Ordner des aktuellen Programms ermitteln

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript den Pfad zum Ordner des aktuellen Programms (über welches das AppleScript ausgeführt wird) ermitteln:

```applescript
tell application "Finder"
  set folderPath to (path to me)'s folder
end tell

-- Ergebnis: folder "Utilities" of folder "Applications" of startup disk of application "Finder"
```
