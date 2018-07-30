---
title: Maßeinheit für Lineale in Adobe Photoshop ermitteln und setzen
---

## Maßeinheit für Lineale in Adobe Photoshop ermitteln und setzen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Maßeinheit für Lineale in Adobe Photoshop (hier in der Version CS3) ermitteln oder setzen möchte, dann kann man dies wie folgt tun:

### Maßeinheit für Lineale ermitteln

```applescript
tell application "Adobe Photoshop CS3"
  get ruler units of settings
end tell
-- Ergebnis: inch units
```

### Maßeinheit für Lineale setzen

```applescript
tell application "Adobe Photoshop CS3"
  set ruler units of settings to inch units
end tell
```

Damit wird folgende Einstellung bearbeitet:

Adobe Photoshop: Voreinstellungen - Maßeinheiten & Lineale

Dabei ist zu beachten, dass während der Ausführung der oben genannten Skripte der "Voreinstellungen"-Dialog von Adobe Photoshop geschlossen sein muss, da es sonst zu einem Script-Fehler kommt.
