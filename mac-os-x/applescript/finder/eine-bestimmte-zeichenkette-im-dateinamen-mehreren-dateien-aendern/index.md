---
title: Eine bestimmte Zeichenkette im Dateinamen mehreren Dateien ändern
---

## Eine bestimmte Zeichenkette im Dateinamen mehreren Dateien ändern

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man viele Dateien hat die im Dateinamen zum Beispiel ein oder mehrere Leerzeichen enthalten und man möchte diese durch einen Unterstrich ("_") ersetzen, dann kann man dies durch AppleScript automatisieren. Dies ist zum Beispiel sehr nützlich, wenn man die Dateien für eine Webseite weiterverwenden möchte - hier ist es immer besser, wenn Dateien keine Leerzeichen enthalten (warum, weshalb und wieso - das würde an dieser Stelle zu weit führen). Hier das script um Leerzeichen durch Unterstrich(e) zu ersetzen:

```applescript
tell application "Finder"
  set target_files to every file of ¬
    (entire contents of (choose folder)) whose name contains " "
  repeat with current_file in target_files
    set new_file_name to my getNewFileName(name of current_file)
    set name of current_file to new_file_name
  end repeat
end tell

on getNewFileName(old_name)
  set {old_delims, my text item delimiters} to ¬
    {my text item delimiters, " "}
  set name_parts to text items of old_name
  set my text item delimiters to "_"
  set new_name to name_parts as string
  set my text item delimiters to old_delims
  return new_name
end getNewFileName
```

Dieses Script kann man natürlich beliebig anpassen um zum Beispiel alle Umlaute durch entsprechende Entities zu ersetzen - auch sehr nützlich für die Weiterverwendung auf einer Webseite aus dem bereits oben genannten Grund. 
