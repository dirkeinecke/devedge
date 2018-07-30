---
title: Zufälliges Element aus Liste auswählen
---

## Zufälliges Element aus Liste auswählen

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man aus einer Liste ein Element nach dem Zufallsprinzip heraussuchen möchte, dann kann man dies wie folgt tun:

```applescript
set theList to {1, 2, 3, 4, 5, 6, 7, 8, 9, 0}
set randomItem to some item of theList
display dialog randomItem buttons ("OK") default button 1
```
