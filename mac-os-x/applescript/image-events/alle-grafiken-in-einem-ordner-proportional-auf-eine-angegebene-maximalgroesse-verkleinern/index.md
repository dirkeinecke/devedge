---
title: Alle Grafiken in einem Ordner proportional auf eine angegebene Maximalgröße verkleinern
---

## Alle Grafiken in einem Ordner proportional auf eine angegebene Maximalgröße verkleinern

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Dieses Script verkleinert alle Grafiken in einem Ordner proportional auf die angegebene Maximalgröße. Die Maximalwerte für Breite und Höhe können unabhängig voneinander definiert werden.

```applescript
(*
Resize images to max size
Copyright © 2006 Dirk Einecke. Alle Rechte vorbehalten.
Mac DevEdge / http://www.mac-devedge.de
*)

(*
Dieses Script verkleinert alle Grafiken in einem Ordner
proportional auf eine angegebene Maximalgröße.
Die Maximalwerte für Breite und Höhe können unabhängig voneinander definiert werden.
*)

-- Erlaubte Datei-Typen festlegen
set file_types_list to {"PICT", "TIFF", "GIFf", "PNGf", "JPEG"}
-- Datei-Typen sind optional, deswegen noch die erlaubten Dateiendungen festlegen
set file_extensions_list to {"pict", "pct", "tif", "tiff", "gif", "png", "jpg", "jpeg"}

-- Maximalgrösse (Breite & Höhe) festlegen
property max_width : 1024
property max_height : 768

set files_total to 0
set files_no_image to 0
set images_resized to 0
set images_to_small to 0

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
  set the_folder to choose folder with prompt "Bitte wählen Sie einen Ordner mit Bildern aus:"
  set the_files to every file of the_folder whose ¬
    file type is in the file_types_list or name extension is in the file_extensions_list
  
  set files_total to the count of the_files
  
  if not files_total = 0 then
    set the_dialog to (display dialog "Es wurden " & (files_total as string) ¬
      & " Dateien zum Verkleinern ausgewählt." & return & return ¬
      & "Dieser Vorgang kann etwas Zeit in Anspruch nehmen." & ¬
      " Sie erhalten eine Meldung, wenn der Vorgang beendet wurde." buttons ¬
      {"Abbrechen", "Weiter"} default button 2)
    set the_button to button returned of the_dialog as text
    
    if the_button = "Weiter" then
      repeat with counter from 1 to the count of the_files
        set the_file to (item counter of the_files) as string
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
              set images_resized to images_resized + 1
            else
              set images_to_small to images_to_small + 1
            end if
          on error
            set files_no_image to files_no_image + 1
          end try
          close the_image
        end tell
      end repeat
      
      display dialog "Der Vorgang wurde beendet. " & return & return ¬
        & "Dateien gesamt: " & tab & tab & tab & files_total & return ¬
        & "Bilder: " & tab & tab & tab & tab & tab & (files_total - files_no_image) & return ¬
        & "Bilder verkleinert: " & tab & tab & images_resized & return ¬
        & "Bilder nicht verkleinert: " & tab & images_to_small ¬
        buttons {"OK"} default button 1
      
    end if
  else
    display dialog "Der Ordner enthält keine Bilder." buttons {"OK"} default button 1 with icon 2
  end if
end tell
```
