---
title: Programmversion ermitteln
---

## Programmversion ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die aktuell installierte Version eines bestimmten Programms ermitteln möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Safari"
  get version
end tell

-- Ergebnis bei mir: "3.0.3"
```

Dabei sollte man beachten, dass das Script das entsprechende Programm zunächst startet. Dies kann manchmal etwas dauern. Wenn nach dem Starten des Programms zum Beispiel fünf Sekunden gewartet werden soll bis das Programm vollständig geladen wurde, dann kann man dies wie folgt tun:

```applescript
tell application "Safari"
  with timeout of 5 seconds
    get version
  end timeout
end tell

-- Ergebnis bei mir: "3.0.3"
```
