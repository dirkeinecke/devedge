---
title: Drücken der ESC-Taste simulieren
---

## Drücken der ESC-Taste simulieren

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn Sie das Drücken der ESC-Taste simulieren möchten, dann können Sie dies wie folgt tun:

```applescript
tell application "System Events" to keystroke ¬
  (ASCII character 27) using ¬
  {option down, command down}
```
