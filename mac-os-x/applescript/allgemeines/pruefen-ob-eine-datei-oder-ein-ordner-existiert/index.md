---
title: Prüfen ob eine Datei oder ein Ordner existiert
---

## Prüfen ob eine Datei oder ein Ordner existiert

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man prüfen möchte, ob eine bestimmte Datei oder ein bestimmter Ordner existiert, dann kann man dies wie folgt tun:

```applescript
set the_path to "/Users/dirkeinecke/Desktop/"

try
  POSIX file (the_path) as alias
  set file_exists to true
on error
  set file_exists to false
end try

-- Ergebnis: true
```
