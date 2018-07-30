---
title: Vollständigen Namen des aktuellen Benutzers anzeigen
---

## Vollständigen Namen des aktuellen Benutzers anzeigen

Getestet mit: Mac OS X 10.6.2 und AppleScript 2.1.1

Wie Sie den vollständigen Namen des aktuellen Benutzers anzeigen können, zeigt Ihnen das folgende Script:

```applescript
set systemInfo to system info
set username to long user name of systemInfo
```
