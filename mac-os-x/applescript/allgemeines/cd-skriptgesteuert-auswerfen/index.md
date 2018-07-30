---
title: CD skriptgesteuert auswerfen
---

## CD skriptgesteuert auswerfen

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man eine CD skriptgesteuert auswerfen möchten, dann kann man dies wie folgt tun. Dabei ist zu beachten, dass "drutil" erst ab Mac OS X 10.3 verfügbar ist.

```applescript
do shell script "drutil tray eject"
```

Möchte man die CD eines entfernten Macs auswerfen, dann kann man dies wie folgt tun. Für dieses Beispiel ist ebenfalls "drutil" erforderlich und es muss in den Systemeinstellungen im Bereich "Sharing" der Dienst "Entfernte Apple Events" aktiviert sein.

```applescript
tell application "Finder" of machine "eppc://192.168.2.32"
  using terms from application "Finder"
    do shell script ("drutil tray eject")
  end using terms from
end tell
```
