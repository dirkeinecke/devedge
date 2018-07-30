---
title: Test ob eine Zahl gerade oder ungerade ist
---

## Test ob eine Zahl gerade oder ungerade ist

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wen man testen möchte, ob eine Zahl gerade oder ungerade ist, dann kann man dies wie folgt tun wobei das Ergebnis "`true`" gerade und "`false`" ungerade bedeutet:

```applescript
set my_number to 4
set my_result to (my_number mod 2 is 0)
-- Ergebnis: true
```

```applescript
set my_number to 5
set my_result to (my_number mod 2 is 0)
-- Ergebnis: false
```
