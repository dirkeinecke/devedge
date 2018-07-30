---
title: Ebene in Adobe Photoshop löschen
---

## Ebene in Adobe Photoshop löschen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man eine Ebene in Adobe Photoshop löschen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Adobe Photoshop CS3"
  tell current document
    -- Diese Funktion ist nicht verfügbar, wenn es nur eine Ebene gibt.
    if (count of layers) > 1 then
      delete (first layer whose name is "Ebene 1")
    end if
  end tell
end tell
```
