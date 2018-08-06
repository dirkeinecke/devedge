---
title: Versteckte Dateien und Ordner einblenden/ausblenden
---

## Versteckte Dateien und Ordner einblenden/ausblenden

Getestet mit: Mac OS X 10.6.2, AppleScript 2.1.1

Das folgende Beispiel zeigt, wie Sie mit Hilfe von AppleScript versteckte Dateien und Ordner im Finder ein- bzw. ausblenden.

### Quellcode

```applescript
display dialog ¬
  "Versteckte Dateien und Ordner..." buttons {"Einblenden", "Ausblenden", "Abbrechen"} ¬
  default button 3

if button returned of result is "Ausblenden" then
  do shell script "defaults write com.apple.finder AppleShowAllFiles -boolean false"
else if button returned of result is "Einblenden" then
  do shell script "defaults write com.apple.finder AppleShowAllFiles -boolean true"
end if

tell application "Finder" to quit
delay 1
tell application "Finder" to activate
```

Screenshot
