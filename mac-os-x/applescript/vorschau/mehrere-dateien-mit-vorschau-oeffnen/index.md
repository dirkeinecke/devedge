---
title: Mehrere Dateien mit "Vorschau" öffnen
---

## Mehrere Dateien mit "Vorschau" öffnen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn Sie mehrere Dateien (zum Beispiel PDFs) mit dem Programm "Vorschau" (Preview.app) öffnen möchten um den Drawer nutzen zu können, dann ist das leider nicht direkt möglich, da "Vorschau" nicht scriptable ist. Wenn "Vorschau" Ihr Default-Programm zum Öffnen von PDFs ist, dann können Sie dieses Problem aber mit einen Umweg über den Finder umgehen. Man muss den Finder dazu nur veranlassen, die gewünschten Dateien zu markieren und dann zu öffnen. Dieses Vorgehen zeigt das folgende Beispiel:

```applescript
tell application "Finder" to select ¬
  {"Macintosh HD:Bild 1.pdf", ¬
    "Macintosh HD:Bild 2.pdf", ¬
    "Macintosh HD:Bild 3.pdf"}
tell application "Finder" to (open selection)
```

Sie können so aber nicht nur PDFs, sondern auch alle anderen Dateiformate öffnen, die das Programm "Vorschau" verarbeiten kann und für die es das Standard-Programm ist. 
