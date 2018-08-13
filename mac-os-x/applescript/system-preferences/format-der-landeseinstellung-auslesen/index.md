---
title: Format der Landeseinstellung auslesen
---

## Format der Landeseinstellung auslesen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man das Format der Landeseinstellungen (Systemeinstellungen -> Landeseinstellungen -> Formate) auslesen möchte, dann kann man dies wie folgt tun:

```applescript
set format to user locale of (get system info)
display dialog format buttons ("OK") default button 1
```

Hat man in den Einstellungen zum Beispiel "Deutschland" ausgewählt, dann gibt das Skript den Wert "de_DE" zurück.
