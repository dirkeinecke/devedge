---
title: Prüfen welche Objekte im Finder-Fenster ausgewählt sind
---

## Prüfen welche Objekte im Finder-Fenster ausgewählt sind

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man prüfen möchte, welche Objekte im Finder-Fenster ausgewählt sind, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
    
  activate
    
  -- die ausgewählten Objekte
  set selected_items to selection
    
  -- Ausgabe nur zur Überprüfung
  repeat with an_item in selected_items
    display dialog (name of an_item) as text buttons ("OK") default button 1
  end repeat
    
end tell
```
