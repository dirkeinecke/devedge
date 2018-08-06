---
title: Finder beenden und neu starten
---

## Finder beenden und neu starten

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man den Finder beenden und gleich danach wieder starten möchte, dann muss man zwischen den beiden Aktionen (Beenden & Starten) eine kleine Pause einlegen. Das folgende Beispiel zeigt dies:

```applescript
tell application "Finder" to quit
delay 1
tell application "Finder" to activate
```
