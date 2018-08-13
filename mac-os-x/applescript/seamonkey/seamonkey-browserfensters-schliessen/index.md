---
title: SeaMonkey-Browserfensters schließen
---

## SeaMonkey-Browserfensters schließen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man das SeaMonkey-Browserfensters schließen möchte, dann benötigt man dazu "System Events", da der Browser keine entsprechende Funktion zur Verfügung stellt.

```applescript
tell application "SeaMonkey"
  activate
  tell application "System Events"
    keystroke "w" using command down
  end tell
end tell
```
