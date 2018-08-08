---
title: Farbraum einer Grafikdatei ermitteln
---

## Farbraum einer Grafikdatei ermitteln

Getestet mit: Mac OS X 10.4.10 und AppleScript 1.10.7

Wenn man den Farbraum (RGB, CMYK, Graustufen) einer Grafikdatei ermitteln möchte, dann kann man dies wie folgt tun:

```applescript
set the_file to (POSIX path of (choose file))
set the_color_space to (do shell script "sips -g space " & the_file)
set {old_delimiters, AppleScript's text item delimiters} to {AppleScript's text item delimiters, ":"}
try
  set the_color to text item 2 of the_color_space as text
end try
set AppleScript's text item delimiters to old_delimiters

display dialog the_color buttons ("OK") default button 1

Das oben genannte Script gehört zwar nicht so richtig in diese Rubrik ("Image Events"), aber ich habe es trotzdem mal mit hier eingeordnet, da die Lösung über "Image Events" zu einem Fehler führt, wenn die Grafik im Farbraum "Graustufen" vorliegt. Die Lösung über "Image Events" funktioniert also nur mit den Farbräumen RGB und CMYK und sei hier nur der Vollständigkeit halber aufgeführt:

set the_file to (choose file)
tell application "Image Events"
  launch
  set this_image to open the_file
  copy the color space of this_image to the_color
  close this_image
end tell

display dialog the_color as string buttons ("OK") default button 1
```
