---
title: URL des SeaMonkey-Browserfensters ermitteln
---

## URL des SeaMonkey-Browserfensters ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die URL des SeaMonkey-Browserfensters ermitteln möchte, dann kann man dies wie folgt tun:

```applescript
tell application "SeaMonkey"
  set theURL to «class curl» of window 1
end tell
-- Ergebnis z.B.: "http://www.seamonkey-project.org/"
```
