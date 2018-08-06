---
title: Ordner öffnen
---

## Ordner öffnen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man einen bestimmten Ordner öffnen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  -- In diesem Beispiel befindet sich der Ordner auf ¬
  -- dem Schreibtisch. Deswegen holen wir uns ¬
  -- erstmal den Pfad zum "Schreibtisch" (desktop).
  set folder_path to path to desktop folder as string
  -- Nun fügen wir noch den Ordnernamen an.
  set folder_path to folder_path & "Ordnername"
  -- Nun öffnen wir den Ordner.
  open folder folder_path
end tell
```
