---
title: URL des Safari-Browserfensters ermitteln
---

## URL des Safari-Browserfensters ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die URL des Safari-Browserfensters ermitteln möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Safari"
  activate
  set the_url to URL of document 1
end tell
-- Ergebnis z. B.: "http://www.apple.com/startpage/"
```
