---
title: Alle minimierten Fenster des Finders öffnen
---

## Alle minimierten Fenster des Finders öffnen

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man alle minimierten (im Dock abgelegten) Fenster des Finders öffnen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  set collapsed of every window to false
end tell
```
