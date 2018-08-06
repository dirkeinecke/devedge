---
title: Spaltenbreite des Finder-Fensters ändern
---

## Spaltenbreite des Finder-Fensters ändern

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Spaltenbreite des Finder-Fensters ändern möchte, dann kann man dies wie folgt tun:

```applescript
tell application "Finder"
    
  activate
  select Finder window 1
    
  -- Zur Darstellung "Objekte als Liste anzeigen" wechseln
  set current view of Finder window 1 to list view
    
  -- Spalte: Name
  set width of column id name column of list view options of Finder window 1 to 300
  -- Spalte: Änderungsdatum
  set width of column id modification date column of list view options of Finder window 1 to 200
  -- Spalte: Größe
  set width of column id size column of list view options of Finder window 1 to 90
  -- Spalte: Art
  set width of column id kind column of list view options of Finder window 1 to 160
    
end tell
```
