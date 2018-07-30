---
title: Umrechnung von px-Wert in em-Wert
---

## Umrechnung von px-Wert in em-Wert

Getestet mit: Mac OS X 10.3.5 und AppleScript 1.9.3

Wenn man häufig die Umrechnung von px-Werte in em-Werte benötigt (zum Beispiel bei der Erstellung von Webseiten) und man nicht ständig zum Rechner greifen möchte um die entsprechenden Operationen auszuführen, dann kann man folgendes script als Programm abspeichern und für den schnellen Zugriff im Dock ablegen.

```applescript
on searchReplace(origStr, searchStr, replaceStr)
  set old_delim to AppleScript's text item delimiters
  set AppleScript's text item delimiters to searchStr
  set origStr to text items of origStr
  set AppleScript's text item delimiters to replaceStr
  set origStr to origStr as string
  set AppleScript's text item delimiters to old_delim
  return origStr
end searchReplace

set text1 to "Bitte geben Sie den Wert in px an, " & ¬
  "der in em umgerechnet werden soll:"

set pxValue to text returned of ¬
  (display dialog text1 default answer "" buttons ¬
    {"OK ", "Abbruch"} default button 1 ¬
    with icon note)

if not pxValue = "" then
  try
    -- px in em Umrechnung
    set emValue to (pxValue / 16)
    -- auf zwei Nachkommastellen runden
    set emValue to (round (emValue * 100)) / 100
    set emValue to ((emValue) as text)
    set emValue to (searchReplace(emValue, ",", "."))
    set text2 to pxValue & "px entspricht " & emValue & "em."
    display dialog text2 buttons ¬
      {"OK", "Clipboard"} default button 1 ¬
      with icon note
    set DialogResult to result
    if button returned of result = "OK" then
      beep 1
    else if button returned of result = "Clipboard" then
      set the clipboard to emValue
      beep 2
    end if
  on error
    set text2 to "Ihre Eingabe war leer oder keine Zahl."
    display dialog text2 buttons ¬
      {"OK"} default button 1 giving up after 5 ¬
      with icon caution
  end try
end if
```
