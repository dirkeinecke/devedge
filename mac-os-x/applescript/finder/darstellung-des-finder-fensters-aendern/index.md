---
title: Darstellung des Finder-Fensters ändern
---

## Darstellung des Finder-Fensters ändern


Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die Darstellung des Finder-Fensters ändern möchte, dann kann man dies wie folgt tun:

### Objekte als Symbole (icon view) anzeigen

```applescript
tell application "Finder"
  activate
  select Finder window 1
  set current view of Finder window 1 to icon view
end tell
```

### Objekte als Liste (list view) anzeigen

```applescript
tell application "Finder"
  activate
  select Finder window 1
  set current view of Finder window 1 to list view
end tell
```

### Objekte in Spalten (column view) anzeigen

```applescript
tell application "Finder"
  activate
  select Finder window 1
  set current view of Finder window 1 to column view
end tell
```

### Mit Mac OS X 10.5 ist die CoverFlow-Ansicht (flow view) hinzugekommen

```applescript
tell application "Finder"
  activate
  select Finder window 1
  set current view of Finder window 1 to flow view
end tell
```
