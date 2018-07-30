---
title: Programm im Vordergrund ermitteln
---

## Programm im Vordergrund ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man ermitteln möchte, welches Programm gerade im Vordergrund ist, dann kann man dies wie folgt tun:

```applescript
short name of (info for (path to frontmost application)) as text
-- Ergebnis: "Script Editor"
```

Eine andere Schreibweise dieser Prüfung ist folgende:

```applescript
short name of (info for (path to «constant afdregfp»)) as text
-- Ergebnis: "Script Editor"
```
