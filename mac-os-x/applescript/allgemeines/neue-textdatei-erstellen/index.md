---
title: Neue Textdatei erstellen
---

## Neue Textdatei erstellen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man eine neue Textdatei erstellen möchte, dann kann man dies wie folgt tun:

```applescript
set new_file to open for access ¬
  file "Macintosh HD:file.txt" with write permission
close access new_file
```

Möchte man nun beim Erstellen der Datei (oder später) etwas in diese Textdatei schreiben, dann kann man dies so machen:

```applescript
set new_file to open for access ¬
  file "Macintosh HD:file.txt" with write permission
write "Hier steht ein beliebiger Text." to new_file
close access new_file
```
