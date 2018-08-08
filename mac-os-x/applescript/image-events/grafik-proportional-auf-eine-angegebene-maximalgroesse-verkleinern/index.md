---
title: Grafik proportional auf eine angegebene Maximalgröße verkleinern
---

## Grafik proportional auf eine angegebene Maximalgröße verkleinern

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Dieses Script verkleinert eine Grafik proportional auf die angegebene Maximalgröße. Die Maximalwerte für Breite und Höhe können unabhängig voneinander definiert werden.

```applescript
(*
Resize image to max size
Copyright © 2006 Dirk Einecke. Alle Rechte vorbehalten.
Mac DevEdge / http://www.mac-devedge.de
*)

(*
Dieses Script verkleinert eine Grafik proportional auf eine angegebene Maximalgröße.
Die Maximalwerte für Breite und Höhe können unabhängig voneinander definiert werden.
*)

-- Erlaubte Datei-Typen festlegen
set file_types_list to {"PICT", "TIFF", "GIFf", "PNGf", "JPEG"}
-- Datei-Typen sind optional, deswegen noch die erlaubten Dateiendungen festlegen
set file_extensions_list to {"pict", "pct", "tif", "tiff", "gif", "png", "jpg", "jpeg"}

-- Maximalgrösse (Breite & Höhe) festlegen
property max_width : 1024
property max_height : 768

set ready_message to "Die Grafik wurde erfolgreich verkleinert."

on check_file_type(the_file, file_types_list, file_extensions_list)
  tell application "Finder"
    set file_type to the file type of the (info for the_file)
    set file_extension to the name extension of the (info for the_file)
    if (file_type is in the file_types_list) or (file_extension is in the file_extensions_list) then
      return true
    else
      return false
    end if
  end tell
end check_file_type

tell application "Finder"
  -- Bild auswählen
  set the_file to choose file with prompt "Bitte wählen Sie eine Grafikdatei aus:"
  -- Dateiname auslesen
  set file_name to the displayed name of the (info for the_file)
end tell

if check_file_type(the_file, file_types_list, file_extensions_list) = true then
  
  tell application "Image Events"
    -- Application starten
    -- (nicht activate verwenden weil "Image Events" kein GUI hat)
    launch
    
    -- Bild laden
    set the_image to open the_file
    
    try
      -- Höhe und Breite des Bildes ermitteln
      set {image_width, image_height} to the dimensions of the_image
      
      -- Wenn das Bild größer ist als die Maximalwerte, dann verkleinern und speichern
      if (image_width > max_width) or (image_height > max_height) then
        
        -- Skalierungsfaktor berechnen
        set scale_factor_width to 100 / image_width * max_width / 100
        set scale_factor_height to 100 / image_height * max_height / 100
        if scale_factor_width < scale_factor_height then
          set scale_factor to scale_factor_width
        else
          set scale_factor to scale_factor_height
        end if
        
        -- Bild skalieren
        scale the_image by factor scale_factor
        
        -- Bild speichern
        save the_image in the_file with icon
        
        display dialog ready_message buttons {"OK"} default button 1
      else
        set ready_message to "Die Grafik \"" & file_name & "\" muss nicht verkleinert werden."
      end if
    on error
      tell application "Finder"
        display dialog "Fehler beim Lesen der Datei \"" & file_name & "\"." buttons ¬
          {"OK"} default button 1 with icon 2
      end tell
    end try
    close the_image
  end tell
else
  display dialog ¬
    "Fehler beim Öffnen der Datei \"" & file_name & "\"." buttons ¬
    {"OK"} default button 1 with icon 2
end if
```
