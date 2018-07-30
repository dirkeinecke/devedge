---
title: Mac OS X Version ermitteln
---

# Mac OS X Version ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man die aktuell verwendete Mac OS X Version ermitteln möchte, dann kann man dies wie folgt tun:

```applescript
set osx_version to system version of (system info)
display dialog osx_version buttons ("OK") default button 1
```applescript

Eine weitere Möglichkeit ist diese:

```applescript
tell application "Finder" to set the_disk to name of startup disk
tell application "System Events"
  set the_file to the_disk & ":System:Library:CoreServices:SystemVersion.plist"
  set osx_version to value of property list item "ProductVersion" of property list file the_file
end tell
display dialog osx_version buttons ("OK") default button 1
```

Bei den nächsten beiden Varianten wird die Aufgabe mit Hilfe von "shell script" realisiert:

```applescript
set osx_version to (do shell script "sw_vers -productVersion")
display dialog osx_version buttons ("OK") default button 1

set osx_version to (do shell script "defaults read /System/Library/CoreServices/SystemVersion ProductUserVisibleVersion")
display dialog osx_version buttons ("OK") default button 1
```
