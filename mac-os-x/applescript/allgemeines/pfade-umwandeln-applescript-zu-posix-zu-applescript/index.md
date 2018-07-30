---
title: Pfade umwandeln: AppleScript zu POSIX zu AppleScript
---

## Pfade umwandeln: AppleScript zu POSIX zu AppleScript

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Möchte man AppleScript-Pfade (zum Beispiel: "`Macintosh HD:Users:dirkeinecke:Desktop:`") in POSIX-Pfade umwandeln, so kann man dies wie folgt tun:

```applescript
POSIX path of file "Macintosh HD:Users:dirkeinecke:Desktop:"
-- Ergebnis: "/Users/dirkeinecke/Desktop/"
```

Möchte man POSIX-Pfade (zum Beispiel "`/Users/dirkeinecke/Desktop/`") in AppleScript-Pfade umwandeln, so kann man dies wie folgt tun:

```applescript
set POSIX_path to "/Users/dirkeinecke/Desktop/"
set AS_path to POSIX file POSIX_path
-- Ergebnis: file "Macintosh HD:Users:dirkeinecke:Desktop:"
```

Diese Umwandlungen können hilfreich sein, wenn man Interaktionen zwischen AppleScript und Shell-Skripts durchführen möchte.

```applescript
set POSIX_path to POSIX path of file "Macintosh HD:Users:dirkeinecke:Desktop:"
do shell script "ls -lisa " & POSIX_path

-- Ergebnis:
--
-- "total 2651344
-- 477087 0 drwx------ 112 dirkeine dirkeine 3808 Nov 9 08:12 .
-- 477076 0 drwxr-xr-x 31 dirkeine dirkeine 1054 Nov 8 16:24 ..
-- 3294035 0 drwxr-xr-x 3 dirkeine dirkeine 102 Apr 20 2007 .BAH802
-- 3294037 0 drwxr-xr-x 3 dirkeine dirkeine 102 Apr 20 2007 .BAH806
-- ...
```
