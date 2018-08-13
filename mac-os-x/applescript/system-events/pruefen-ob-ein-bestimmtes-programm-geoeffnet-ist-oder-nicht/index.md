---
title: Prüfen ob ein bestimmtes Programm geöffnet ist oder nicht
---

## Prüfen ob ein bestimmtes Programm geöffnet ist oder nicht

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man prüfen möchte, ob ein bestimmtes Programm (in diesem Beispiel "Safari") geöffnet ist oder nicht, dann kann man dies wie folgt tun.

### Möglichkeit #1

```applescript
tell application "System Events"
  if exists application process "Safari" then
    display dialog "Safari ist aktiv." buttons ("OK") default button 1
  else
    display dialog "Safari ist nicht aktiv." buttons ("OK") default button 1
  end if
end tell
```

### Möglichkeit #2

```applescript
tell application "System Events"
  if (process "Safari") exists then
    display dialog "Safari ist aktiv." buttons ("OK") default button 1
  else
    display dialog "Safari ist nicht aktiv." buttons ("OK") default button 1
  end if
end tell
```

### Möglichkeit #3

```applescript
tell application "System Events"
  if (application processes whose name is "Safari") is not {} then
    display dialog "Safari ist aktiv." buttons ("OK") default button 1
  else
    display dialog "Safari ist nicht aktiv." buttons ("OK") default button 1
  end if
end tell
```

### Möglichkeit #4

```applescript
on check_app_exists(my_app)
  tell application "System Events" to get name of every process
  if result contains my_app then return true
  return false
end check_app_exists

my check_app_exists("Safari")
-- Ergebnis: true
```
