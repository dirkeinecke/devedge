---
title: URL des Firefox-Browserfensters ermitteln
---

## URL des Firefox-Browserfensters ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die URL des Firefox-Browserfensters ermitteln möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Firefox"
  set theURL to «class curl» of window 1
end tell
-- Ergebnis z. B.: "http://www.mozilla-europe.org/de/"
```
