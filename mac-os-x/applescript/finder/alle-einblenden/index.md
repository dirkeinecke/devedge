---
title: Alle einblenden
---

## Alle einblenden

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Funktionalität "Alle einblenden" des Finders per AppleScript ausführen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  set visible of processes to true
end tell
```
