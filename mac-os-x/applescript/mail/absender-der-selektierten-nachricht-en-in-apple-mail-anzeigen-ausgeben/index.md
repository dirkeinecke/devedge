---
title: Absender der selektierten Nachricht(en) in Apple Mail anzeigen / ausgeben
---

## Absender der selektierten Nachricht(en) in Apple Mail anzeigen / ausgeben

Getestet mit: Mac OS X 10.4.8 und AppleScript 1.10.7

Wenn man sich den Absender der selektierten Nachricht(en) in Apple Mail anzeigen beziehungsweise ausgeben lassen möchte, dann kann man dies wie folgt tun:

```applescript
(*
Get Sender From Selection
Copyright © 2006 Dirk Einecke. Alle Rechte vorbehalten.
*)

set carriageReturn to return as text

set messagesList to {}
set senderList to {}
set output to ""

try
  tell application "Mail"
    activate
    -- Alle ausgewählten E-Mails holen
    set messagesList to selection
  end tell
  
  -- Wenn E-Mails ausgewählt wurden
  if not ((count of messagesList) = 0) then
    -- Liste der ausgewählen E-Mails durchgehen
    repeat with counter from 1 to the count of messagesList
      set currentMessage to (item counter of messagesList)
      tell application "Mail"
        -- Absender der aktuellen E-Mail holen
        set theSender to sender of currentMessage as string
        -- Absender in die Liste "senderList" schreiben
        set senderList to senderList & theSender
      end tell
    end repeat
    
    -- Aus der Liste "senderList" einen String erzeugen
    -- Nach jedem Absender wird ein Zeilenumbruch eingefügt
    repeat with i from 1 to count of senderList
      set output to output & (item i of senderList) & carriageReturn
    end repeat
    
    -- Liste (String mit Zeilenumbrüchen) in ein neues TextEdit-Dokument schreiben
    tell application "TextEdit"
      activate
      -- Neues TextEdit-Dokument erzeugen
      tell application "TextEdit" to make new document at end of documents
      -- Liste in das Dokument einfügen
      tell application "TextEdit" to set text of document 1 to output
    end tell
    
  else
    -- Wenn keine E-Mails ausgewählt wurde erscheint ein entsprechender Hinweis
    display dialog "Sie haben keine E-Mail ausgewählt." buttons ¬
      {" OK "} default button 1 ¬
      with icon caution
  end if
end try
```
