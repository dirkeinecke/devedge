---
title: Dateiname des aktuellen Programms ermitteln
---

## Dateiname des aktuellen Programms ermitteln

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript den Dateinamen des aktuellen Programms (über welches das AppleScript ausgeführt wird) ermitteln.

### Beispiel #1

```applescript
tell application "Finder"
  set myName to name of (path to me)
end tell

-- Ergebnis: folder "AppleScript Editor.app"
```

### Beispiel #2

```applescript
tell application "Finder"
  set myPath to path to me
  set myName to name of item myPath
end tell

-- Ergebnis: folder "AppleScript Editor.app"
```
