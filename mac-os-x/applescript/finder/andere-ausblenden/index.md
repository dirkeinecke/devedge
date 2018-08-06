---
title: Andere ausblenden
---

## Andere ausblenden

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Funktionalität "Andere ausblenden" des Finders per AppleScript ausführen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  set visible of processes to false
end tell
```
