---
title: Etikett (Label) für Objekte setzen
---

## Etikett (Label) für Objekte setzen

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man ein Etikett (Label) für Objekte setzen im Finder-Fenster setzen möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
  activate
  select Finder window 1
  set label index of every item of Finder window 1 to 5 -- 5 = Violett
end tell
```

In diesem Beispiel wird das Etikett auf die Farbe "violett" (Index 5) gesetzt.

Folgende Farben stehen zur Verfügung:

| Index | Farbe |
|-------|-------|
| 0 | keine Farbe |
| 1 | Orange |
| 2 | Rot |
| 3 | Gelb |
| 4 | Blau |
| 5 | Violett |
| 6 | Grün |
| 7 | Grau |
