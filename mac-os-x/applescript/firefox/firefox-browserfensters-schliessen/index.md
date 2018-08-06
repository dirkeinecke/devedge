---
title: Firefox-Browserfensters schließen
---

## Firefox-Browserfensters schließen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man das Firefox-Browserfensters schließen möchte, dann benötigt man dazu "System Events", da der Browser keine entsprechende Funktion zur Verfügung stellt.

```applescript
tell application "Firefox"
  activate
  tell application "System Events"
    keystroke "w" using command down
  end tell
end tell
```
