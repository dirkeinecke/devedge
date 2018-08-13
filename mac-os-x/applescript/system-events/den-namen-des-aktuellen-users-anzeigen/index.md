---
title: Den Namen des aktuellen Users anzeigen
---

## Den Namen des aktuellen Users anzeigen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wie Sie den Namen des aktuellen Users anzeigen können, zeigt ihnen das folgende Script:

```applescript
tell application "System Events"
  set username to full name of current user
  display dialog username buttons ¬
    {"OK"} default button 1
end tell
```
