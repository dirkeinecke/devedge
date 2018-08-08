---
title: Listen (lists)
---

## Listen (lists)

Die folgenden Beispiele zeigen dem Umgang mit Listen (lists).

- Listen werden in geschweifte Klammern (`{}`) eingeschlossen.
- Ist ein Listenelement ein String, dann muss er durch Anführungszeichen (`""`) eingeschlossen werden.
- Einzelne Listenelemente werden durch ein Komma (`,`) getrennt.

### Eine Liste mit zwei Strings definieren

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
-- Ergebnis: {"Mac DevEdge", "Einfach mal weiterdenken."}
```

### Testen ob der Inhalt einer Variablen eine Liste ist

```applescript
set myList to {"a", "b", "c", "d", "e"}
if class of myList is list then
  display dialog "Ist eine Liste" buttons ("OK") default button 1
else
  display dialog "Ist keine Liste" buttons ("OK") default button 1
end if
```

### Eine Liste mit Strings und Zahlen definieren

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken.", 10, 23.5}
-- Ergebnis: {"Mac DevEdge", "Einfach mal weiterdenken.", 10, 23.5}
```

### Eine Liste aus einen Variablenwert (string), einem String und Zahlen definieren

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
set myList to {myString, "Ein String", 10, 23.5}
-- Ergebnis: {"Mac DevEdge - Einfach mal weiterdenken.", "Ein String", 10, 23.5}
```

hier

### Zwei Listen kombinieren

```applescript
set myList1 to {"Mac DevEdge"}
set myList2 to {"Einfach mal weiterdenken."}
set myList to myList1 & myList2
-- Ergebnis: {"Mac DevEdge", "Einfach mal weiterdenken."}
```

### Einen Listeneintrag (item) am Anfang hinzufügen - Variante 1

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set myList's beginning to "www.mac-devedge.de"
get myList
-- Ergebnis: {"www.mac-devedge.de", "Mac DevEdge", "Einfach mal weiterdenken."}
```

### Einen Listeneintrag (item) am Anfang hinzufügen - Variante 2

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set beginning of myList to "www.mac-devedge.de"
get myList
-- Ergebnis: {"www.mac-devedge.de", "Mac DevEdge", "Einfach mal weiterdenken."}
```

### Einen Listeneintrag (item) am Ende hinzufügen - Variante 1

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set myList's end to "www.mac-devedge.de"
get myList
-- Ergebnis: {"Mac DevEdge", "Einfach mal weiterdenken.", "www.mac-devedge.de"}
```

### Einen Listeneintrag (item) am Ende hinzufügen - Variante 2

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set end of myList to "www.mac-devedge.de"
get myList
-- Ergebnis: {"Mac DevEdge", "Einfach mal weiterdenken.", "www.mac-devedge.de"}
```

### Einen Listeneintrag (item) ändern - Variante 1 (empfohlen)

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set item 2 of myList to "www.mac-devedge.de"
get myList
-- Ergebnis: {"Mac DevEdge", "www.mac-devedge.de"}
```

### Einen Listeneintrag (item) ändern - Variante 2

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set 2nd item of myList to "www.mac-devedge.de"
get myList
-- Ergebnis: {"Mac DevEdge", "www.mac-devedge.de"}
```

### Einen Listeneintrag (item) ändern - Variante 3

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set second item of myList to "www.mac-devedge.de"
get myList
-- Ergebnis: {"Mac DevEdge", "www.mac-devedge.de"}
```

### Ersten Listeneintrag (item) bestimmen - Variante 1

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set myFirstItem to the first item of myList
-- Ergebnis: "Mac DevEdge"
```

### Ersten Listeneintrag (item) bestimmen - Variante 2

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set myFirstItem to myList's beginning
-- Ergebnis: "Mac DevEdge"
```

### Mittleren Listeneintrag (item) bestimmen

```applescript
set myList to {"a", "b", "c"}
set myMiddleItem to myList's middle item
-- Ergebnis: "b"

set myList to {"a", "b", "c", "d"}
set myMiddleItem to myList's middle item
-- Ergebnis: "b"

set myList to {"a", "b", "c", "d", "e", "f"}
set myMiddleItem to myList's middle item
-- Ergebnis: "c"
```

### Letzten Listeneintrag (item) bestimmen - Variante 1

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set myLastItem to the last item of myList
-- Ergebnis: "Einfach mal weiterdenken."
```

### Letzten Listeneintrag (item) bestimmen - Variante 2

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set myLastItem to myList's end
-- Ergebnis: "Einfach mal weiterdenken."
```

### Letzten Listeneintrag (item) bestimmen - Variante 3

```applescript
set myList to {"Mac DevEdge", "Einfach mal weiterdenken."}
set myLastItem to item -1 of myList
-- Ergebnis: "Einfach mal weiterdenken."
```

### Teilliste aus einer Liste extrahieren - Variante 1

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set myNewList to items 3 through 6 of myList
-- Ergebnis: {"c", "d", "e", "f"}
```

### Teilliste aus einer Liste extrahieren - Vatiante 2

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set myNewList to items 3 thru 6 of myList
-- Ergebnis: {"c", "d", "e", "f"}
```

### Reihenfolge der Listenelemente umkehren

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set myNewList to reverse of myList
-- Ergebnis: {"j", "i", "h", "g", "f", "e", "d", "c", "b", "a"}
```

### Anzahl der Listeneinträge zählen - Variante 1

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set myQuantity to the length of myList
-- Ergebnis: 10
```

### Anzahl der Listeneinträge zählen - Variante 2

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set myQuantity to the count of myList
-- Ergebnis: 10
```

### Zufälligen Listeneintrag (item) bestimmen

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set myRandomItem to some item of myList
-- Ergebnis kann sein: "b"
```

### Prüfen ob sich ein bestimmter Eintrag in einer Liste befinden - Variante 1

```applescript
set myList to {"a", "b", "c", "d", "e"}
if "a" is in myList then
  display dialog "Der Buchstabe 'a' ist in der Liste enthalten."
end if
```

### Prüfen ob sich ein bestimmter Eintrag in einer Liste befindet - Variante 2

```applescript
set myList to {"a", "b", "c", "d", "e"}
if myList contains {"a"} then
  display dialog "Der Buchstabe 'a' ist in der Liste enthalten."
end if
```

### Prüfen ob die Werte einer Liste - in gleicher Reigenfolge - in einer anderen Liste enthalten sind

```applescript
set myList to {"a", "b", "c", "d", "e"}
-- In der nächsten Zeile kommt es auf die Reihenfolge an: {"a", "b"}
if myList contains {"a", "b"} then
  display dialog "Die Buchstaben 'a' und 'b' sind in der Liste enthalten." buttons ¬
    ("OK") default button 1
end if

set myList to {"a", "b", "c", "d", "e"}
-- In der nächsten Zeile kommt es auf die Reihenfolge an: {"b", "a"}
if myList contains {"b", "a"} then
  display dialog "Die Buchstaben 'b' und 'a' sind in der Liste in " & ¬
    "dieser Reihenfolge enthalten." buttons ¬
    ("OK") default button 1
else
  display dialog "Die Buchstaben 'b' und 'a' sind in der Liste in " & ¬
    "dieser Reihenfolge nicht enthalten." buttons ¬
    ("OK") default button 1
end if
```

### String in eine Liste umwandeln, wobei der gesamte String zu einem einzigen Listeneintrag (item) wird

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
set myList to myString as list
-- Ergebnis: {"Mac DevEdge - Einfach mal weiterdenken."}
```

### String in eine Liste umwandeln, wobei jedes Zeichen des Strings ein einzelner Listeneintrag (item) wird

```applescript
set myString to "Mac DevEdge"
set myList to every character of myString
-- Ergebnis: {"M", "a", "c", " ", "D", "e", "v", "E", "d", "g", "e"}
```

### String in eine Liste umwandeln, wo bei jedes Wort des Strings ein einzelner Listeneintrag (item) wird

```applescript
set myString to "Einfach mal weiterdenken"
set oldDelimiters to AppleScript's text item delimiters
set AppleScript's text item delimiters to " "
set myList to every text item of myString
set AppleScript's text item delimiters to oldDelimiters
get myList
-- Ergebnis: {"Einfach", "mal", "weiterdenken"}
```

### Liste in einen String umwandeln

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set myString to myList as string
-- Ergebnis: "a b c d e f g h i j"
```

### Liste in einen String umwandeln, wobei man das Trennzeichen selbst definiert:

```applescript
set myList to {"a", "b", "c", "d", "e", "f", "g", "h", "i", "j"}
set oldDelimiters to AppleScript's text item delimiters
set AppleScript's text item delimiters to " - "
set myString to myList as string
set AppleScript's text item delimiters to oldDelimiters
get myString
-- Ergebnis: "a - b - c - d - e - f - g - h - i - j"
```

### Routinen (handler)

#### Doppelte Listeneinträge entfernen - Variante 1 (Reihenfolge wird beibehalten)

```applescript
on list_unique(the_list)
    
  -- Neue Liste für die Rückgabe definieren
  set my_new_list to {}
    
  -- Jedes Item der bestehenden Liste durchlaufen
  repeat with counter from 1 to count the_list
        
    -- Neu zu setzenden Listeneintrag definieren
    set new_item to item counter of the_list
        
    -- Den neuen Listeneintrag nur dann an das Ende der
    -- neuen Liste hinzufügen, wenn er noch nicht enthalten ist
    considering case
      if new_item is not in my_new_list then
        set end of my_new_list to new_item
      end if
    end considering
        
  end repeat
    
  -- Neue Liste zurückgeben
  return my_new_list
    
end list_unique

--
-- Anwendungsbeispiele
--

set my_list to {"a", "b", 10, "c", "a", "c", 10}
set my_list to list_unique(my_list)
-- Ergebnis: {"a", "b", 10, "c"}

set my_list to {"a", "b", 10, "c", "a", "C", 10}
set my_list to list_unique(my_list)
-- Ergebnis: {"a", "b", 10, "c", "C"}
--
-- Der Listeneintrag "C" wurde aus der Liste nicht gelöscht,
-- da der Handler "list_unique" case sensitive arbeitet.
```

#### Doppelte Listeneinträge entfernen - Variante 2 (Reihenfolge wird nicht beibehalten)

```applescript
on list_unique(the_list)
    
  -- Neue Liste für die Rückgabe definieren
  set new_list to {}
    
  -- Jedes Item der bestehenden Liste durchlaufen
  repeat until the_list = {}
        
    -- Ersten Listeneintrag holen
    set first_item to (first item of the_list)
        
    -- Original-Liste mit dem Rest (ausser ersten Eintrag)
    set the_list to (rest of the_list)
        
    -- Den neuen Listeneintrag nur dann an das Ende der
    -- neuen Liste hinzufügen, wenn er noch nicht enthalten ist
    considering case
      if first_item is not in the_list then
        set new_list to new_list & {first_item}
      end if
    end considering
  end repeat
    
  -- Neue Liste zurückgeben
  return new_list
    
end list_unique

--
-- Anwendungsbeispiel
--

set my_list to {"a", "b", 10, "c", "a", "C", 10}
set my_list to list_unique(my_list)
-- Ergebnis: {"b", "c", "a", "C", 10}
```

#### Eintrag / Einträge aus Liste entfernen

```applescript
on list_delete_items(the_list, the_items)
    
  -- Neue Liste für die Rückgabe definieren
  set my_new_list to {}
    
  -- Jedes Item der bestehenden Liste durchlaufen
  repeat with counter from 1 to count the_list
        
    -- Neu zu setzenden Listeneintrag definieren
    set new_item to item counter of the_list
        
    -- Der neue Listeneintrag wird nur dann an das Ende der
    -- neuen Liste hinzugefügt, wenn er nicht in der "Ausschlussliste" enthalten ist.
    considering case
      if new_item is not in the_items then
        set end of my_new_list to new_item
      end if
    end considering
        
  end repeat
    
  -- Neue Liste zurückgeben
  return my_new_list
    
end list_delete_items

--
-- Anwendungsbeispiele
--

set my_list to {1, 2, 3, 4, "Mac DevEdge", 5, 6, 7, 8, 9}
set my_list to list_delete_items(my_list, {"Mac DevEdge"})
-- Ergebnis: {1, 2, 3, 4, 5, 6, 7, 8, 9}

set my_list to {1, 2, 3, 4, "Mac DevEdge", 5, 6, 7, 8, 9}
set my_list to list_delete_items(my_list, {"mac devedge"})
-- Ergebnis: {1, 2, 3, 4, "Mac DevEdge", 5, 6, 7, 8, 9}
--
-- "mac devedge" wurde aus der Liste nicht gelöscht,
-- da der Handler "list_delete_items" case sensitive arbeitet.

set my_list to {1, 2, 3, 4, "Mac", 5, 6, "DevEdge", 7, 8, 9}
set my_list to list_delete_items(my_list, {"Mac", "DevEdge"})
-- Ergebnis: {1, 2, 3, 4, 5, 6, 7, 8, 9}
```
