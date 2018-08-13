---
title: Betreff der selektierten Nachricht in Apple Mail anzeigen / ausgeben
---

## Betreff der selektierten Nachricht in Apple Mail anzeigen / ausgeben

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man sich den Betreff der selektierten Nachricht in Apple Mail anzeigen beziehungsweise ausgeben lassen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Mail"
  set messagesList to selected messages of message viewer 1
  set messageSubject to subject of (item 1 of messagesList)
  display dialog messageSubject
end tell
```
