---
title: Pfad zum Schreibtisch (Desktop)
---

## Pfad zum Schreibtisch (Desktop)

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man den Pfad zum Schreibtisch (Desktop) benötigt, dann kann man dies wie folgt tun:

```applescript
path to desktop
-- Ergebnis: alias "Macintosh HD:Users:dirkeinecke:Desktop:"
```

Aber: Dies ist so nicht ganz richtig, denn dies funktioniert innerhalb eines "tell"-Blocks nicht!

```applescript
-- Dies verursacht einen Fehler!
tell application "Finder"
  path to desktop
end tell
```

Es wird folgender Fehler verursacht:

```
"Finder" hat einen Fehler erhalten: desktop kann nicht in Typ constant umgewandelt werden.
```

Der Finder erwartet diese Schreibweise - mit "folder":

```applescript
tell application "Finder"
  path to desktop folder
end tell
-- Ergebnis: alias "Macintosh HD:Users:dirkeinecke:Desktop:"
```
