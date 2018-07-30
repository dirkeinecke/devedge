---
title: Zeichenkette an Trennzeichen zerlegen
---

## Zeichenkette an Trennzeichen zerlegen

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man eine Zeichenkette anhand eines Trennzeichens zerlegen möchte, dann kann man das wie folgt tun:

```applescript
-- Zeichenkette definieren
set my_text to "12,3"
-- Trennzeichen festlegen
set Applescript's text item delimiters to ","
-- Ersten und zweiten Teil der Zeichenkette ermitteln
set my_first to text item 1 of my_text
set my_last to text item 2 of my_text
-- Trennzeichen zurücksetzen
set Applescript's text item delimiters to ""
-- ersten und zweiten Teil der Zeichenkette ausgeben
display dialog my_first
display dialog my_last
```

Wenn man die Anzahl der Teile nicht vorhersehen kann, dann ist es sinnvoller, mittels "`repeat`" die einzelnen Teile der Zeichenkette herauszufinden. Denn möchte man den zweiten Teil der Zeichenkette ausgeben und es gibt keinen zweiten Teil, so würde es hier zu einem Fehler bei der Ausführung des Programms kommen. Hier nun also ein Lösungsbeispiel mit Hilfe von "`repeat`":

```applescript
-- Zeichenkette definieren
set my_text to "12,3"
-- Trennzeichen festlegen
set Applescript's text item delimiters to ","
-- Zählen der Zeichenkettenbestandteile,
-- die durch ein Trennzeichen getrennt sind
set item_count to (count text items of my_text)
-- Alle Zeichenkettenbestandteile durchlaufen
-- und deren Inhalt ausgeben
repeat with counter from 1 to item_count
display dialog (text item counter of my_text)
end repeat
-- Trennzeichen zurücksetzen
set Applescript's text item delimiters to ""
```

Wenn man nun die Ausgabe etwas schöner gestalten möchte um zum Beispiel die Ursprungszeichenkette und alle Teile in einer Dialogbox anzuzeigen, dann kann man dies wie folgt realisieren:

```applescript
set out to ""
-- Zeichenkette definieren
set my_text to "12,3"
-- Trennzeichen festlegen
set Applescript's text item delimiters to ","
-- Zählen der Zeichenkettenbestandteile,
-- die durch ein Trennzeichen getrennt sind
set item_count to (count text items of my_text)
-- Alle Zeichenkettenbestandteile durchlaufen
-- und den Wert in eine Variable speichern
repeat with counter from 1 to item_count
set out to out & "Teil " & counter & ¬
": " & (text item counter of my_text) & return
end repeat
-- Trennzeichen zurücksetzen
set Applescript's text item delimiters to ""
-- Ausgabe zusammenstellen
set out to "Zeichenkette: " & my_text & return & return & out
-- Ausgabe in einer Dialogbox
display dialog out
```
