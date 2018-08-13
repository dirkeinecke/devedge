---
title: Signaturen aus den Einstellungen von Apple Mail auslesen
---

## Signaturen aus den Einstellungen von Apple Mail auslesen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Signaturen aus den Einstellungen von Apple Mail auslesen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Mail"
  set the_signatures to content of every signature
end tell
```
