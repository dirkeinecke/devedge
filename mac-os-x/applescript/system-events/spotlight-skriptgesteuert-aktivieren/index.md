---
title: Spotlight skriptgesteuert aktivieren
---

## Spotlight skriptgesteuert aktivieren

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man das Spotlight-Suchfeld skriptgesteuert aktivieren möchte, dann kann man dies wie folgt tun:

```applescript
tell application "System Events"
  tell process "Finder"
    activate
    set frontmost to true
    keystroke " " using {command down}
  end tell
end tell
```

Um das Spotlight-Fenster zu öffnen kann man so vorgehen, wie es das folgende Beispiel zeigt:

```applescript
tell application "System Events"
  tell process "Finder"
    activate
    set frontmost to true
    keystroke " " using {option down, command down}
  end tell
end tell
```
