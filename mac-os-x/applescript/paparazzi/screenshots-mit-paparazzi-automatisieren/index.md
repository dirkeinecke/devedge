---
title: Screenshots mit Paparazzi! automatisieren
---

## Screenshots mit Paparazzi! automatisieren

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man das Erstellen von Screenshots mit dem Programm Paparazzi! automatisieren möchte, dann kann man das so tun, wie es das folgende Beispiel zeigt.

Dabei wird zunächst geprüft, ob das Programm Paparazzi! überhaupt installiert ist. Danach wird über eine einfache Dialogbox der URL der Site von der ein Screenshot erstellt werden soll abgefragt. Danach wird automatisch ein Screenshot in der Größe 1024x768 Pixel erstellt und als JPEG-Datei auf dem Schreibtisch gespeichert.

```applescript
(*
Make Screenshot with Paparazzi!
Copyright © 2006 Dirk Einecke. Alle Rechte vorbehalten.
*)

-- Optionen für das Programm "Paparazzi!" definieren
set cropSize to {1024, 768}
set minSize to {1025, 768}

-- Datumswerte für den Dateinamen des Screenshots
set myDate to (current date)
set myDateYear to myDate's year as text
set myDateMonth to myDate's month as text
set myDateDay to myDate's day as text
set myDateHour to myDate's hours as text
set myDateMinute to myDate's minutes as text
set myDateSecond to myDate's seconds as text

set startupDisk to path to startup disk as text
set userName to (do shell script "id -un")
set paparazziCreatorType to "Pzi!"
set paparazziExists to "no"

-- Überprüfen, ob das Programm "Paparazzi!" installiert ist.
try
  tell application "Finder" to application file id "Pzi!"
  set paparazziExists to "yes"
on error
  display dialog "Das Programm Paparazzi! ist nicht installiert." buttons ¬
    {"OK"} default button 1 giving up after 5 ¬
    with icon caution
end try

-- Mit dem Programm nur weitermachen,
-- wenn das Programm "Paparazzi!" installiert ist.
if paparazziExists = "yes" then
  set theDialog to (display dialog "Bitte geben Sie einen URL ein:" default answer "http://" buttons ¬
    {"Abbrechen", "Weiter"} default button 2)
  
  set theButton to button returned of theDialog as text
  set theUrl to text returned of theDialog as text
  
  if theButton = "Weiter" and not theUrl = "http://" and not theUrl = "" then
    tell application "Paparazzi!"
      capture theUrl crop size cropSize min size minSize delay 0
      repeat while busy
        delay 1
      end repeat
      set fileName to (myDateYear & "-" & myDateMonth & "-" & myDateDay & ¬
        "-" & myDateHour & "-" & myDateMinute & "-" & myDateSecond) as text
      save in file (startupDisk & "Users:" & userName & ":Desktop:screenshot-" & fileName & ".jpg") ¬
        as JPEG with icon
      display dialog "Der Screenshot wurde erstellt." buttons ¬
        {"OK"} default button 1 giving up after 5
    end tell
    quit application "Paparazzi!"
  end if
end if
```
