---
title: Wechselmedien auf dem Schreibtisch ausblenden
---

## Wechselmedien auf dem Schreibtisch ausblenden

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man Wechselmedien auf dem Schreibtisch ausblenden möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  tell Finder preferences
    set desktop shows removable media to false
  end tell
end tell
```

Dies hat den selben Effekt wie wenn man bei den Einstellungen ("Allgemein") des Finders die Checkbox "CDs, DVDs und iPods" deaktiviert.

![Einstellungen des Finders](Wechselmedien-auf-dem-Schreibtisch-ausblenden.jpg)

Möchte man die Wechselmedien auf dem Schreibtisch wieder einblenden, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  tell Finder preferences
    set desktop shows removable media to true
  end tell
end tell
```
