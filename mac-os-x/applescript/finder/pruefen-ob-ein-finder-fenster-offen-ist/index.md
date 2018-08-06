---
title: Prüfen ob ein Finder-Fenster offen ist
---

## Prüfen ob ein Finder-Fenster offen ist

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man prüfen möchte, ob ein Finder-Fenster offen ist, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  activate
  tell Finder window 1 to if exists then
    display dialog "Es ist mindestens ein Finder-Fenster offen." buttons ("OK") default button 1
  else
    display dialog "Es ist kein Finder-Fenster offen." buttons ("OK") default button 1
  end if
end tell
```
