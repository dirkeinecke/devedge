---
title: URL aus .webloc-Datei auslesen
---

## URL aus .webloc-Datei auslesen

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man den URL aus einer .webloc-Datei (wird erstellt wenn man aus Safari den URL zum Beispiel auf den Schreibtisch zieht) auslesen möchte, dann kann man dies wie folgt tun:

```applescript
set the_file to choose file
try
  tell application "Finder"
    set the_location to location of file the_file
    display dialog the_location buttons {"OK"} default button 1
  end tell
end try
```
