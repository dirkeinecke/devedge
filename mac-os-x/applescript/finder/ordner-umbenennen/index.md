---
title: Ordner umbenennen
---

## Ordner umbenennen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man einen Ordner umbenennen möchte, dann kann man dies so realisieren, wie es das folgende Script zeigt. Dabei wird davon ausgegangen, dass sich der Ordner auf dem Schreibtisch (`desktop`) befindet.

```applescript
tell application "Finder"
  set name of folder "Neuer Ordner" of desktop to "Neuer Name"
end tell
```

Würde sich der Ordner im Root der Festplatte (`disk`) "Macintosh HD" befinden, dann sieht das Script wie folgt aus:

```applescript
tell application "Finder"
  set name of folder "Neuer Ordner" of disk "Macintosh HD" to "Neuer Name"
end tell
```
