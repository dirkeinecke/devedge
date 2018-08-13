---
title: Tastenkombination Command + Buchstabe ausführen
---

## Tastenkombination Command + Buchstabe ausführen

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1

Das folgende Beispiel zeigt, wie Sie die Tastenkombination Command + Buchstabe (Command + f) ausführen:

```applescript
tell application "System Events" to keystroke ¬
  "f" using {command down}
```

Bei diesem Beispiel wird das Suche-Fenster des aktuellen Programms aufgerufen.
