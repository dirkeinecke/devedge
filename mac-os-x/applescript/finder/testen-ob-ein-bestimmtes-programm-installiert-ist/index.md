---
title: Testen ob ein bestimmtes Programm installiert ist
---

## Testen ob ein bestimmtes Programm installiert ist

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man testen möchte, ob ein bestimmtes Programm installiert ist, dann kann man dies wie folgt tun:

```applescript
set the_application to ("Safari" as string)
set the_application_path to ((path to applications folder) as string) & the_application

tell application "Finder"
  if not (exists alias the_application_path) then
    display dialog "Das Programm \"" & the_application & "\" ist nicht installiert."
  else
    display dialog "Das Programm \"" & the_application & "\" ist installiert."
  end if
end tell

In diesem Beispiel wird beispielhaft geprüft, ob der Apple Browser "Safari" vorhanden ist. Dabei geht das Script davon aus, dass sich das Programm im dafür vorgesehenden Standard-Programme-Verzeichnis von Mac OS X befindet.
```
