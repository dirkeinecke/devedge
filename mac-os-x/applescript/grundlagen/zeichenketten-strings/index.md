---
title: Zeichenketten (strings)
---

## Zeichenketten (strings)

Die folgenden Beispiele zeigen dem Umgang mit Zeichenketten (strings). Beachten Sie dabei immer, dass Strings in Anführungszeichen (`""`) eingeschlossen sein müssen.

### Einen String definieren

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
```

### Testen ob der Inhalt einer Variablen ein String ist

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
if class of myString is in {string, Unicode text} then
  display dialog "Ist ein String" buttons ("OK") default button 1
else
  display dialog "Ist kein String" buttons ("OK") default button 1
end if
```

### Mehrere Strings miteinander verknüpfen

```applescript
set myString to "Mac DevEdge" & " - " & "Einfach mal weiterdenken."
-- Ergebnis: "Mac DevEdge - Einfach mal weiterdenken."

set myString1 to "Mac DevEdge"
set myString2 to "Einfach mal weiterdenken."
set myString to myString1 & " - " & myString2
-- Ergebnis: "Mac DevEdge - Einfach mal weiterdenken."
```

### Die Länge eines Strings bestimmen - Variante 1

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
set theLength to the length of myString
-- Ergebnis: 39
```

### Die Länge eines Strings bestimmen - Variante 2 (besser weil schneller)

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
set theLength to count of myString
-- Ergebnis: 39
```

### Anführungszeichen innerhalb eines Strings

```applescript
set myString to "Ich sage \"Mac DevEdge - Einfach mal weiterdenken.\""
```

### Umwandlung (Coercion) eines Strings in eine Zahl

```applescript
set myNumber to "10" as number
-- Ergebnis: 10
```

### Umwandlung (Coercion) einer Zahl in einen String

```applescript
set myString to 10 as string
-- Ergebnis: "10"
```

### Prüfen ob ein String in einem anderen String enthalten ist - Variante 1

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
if myString contains "DevEdge" then
  display dialog "Ist enhalten" buttons ("OK") default button 1 -- trifft zu
else
  display dialog "Ist nicht enthalten" buttons ("OK") default button 1
end if
```

### Prüfen ob ein String in einem anderen String enthalten ist - Variante 2

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
if "DevEdge" is in myString then
  display dialog "Ist enhalten" buttons ("OK") default button 1 -- trifft zu
else
  display dialog "Ist nicht enthalten" buttons ("OK") default button 1
end if
```

### Prüfen wie oft ein String in einem anderen String enthalten ist

```applescript
set myString1 to "Mac DevEdge - Einfach mal weiterdenken."
set myString2 to "n"

set {oldDelimiters, AppleScript's text item delimiters} to {AppleScript's text item delimiters, myString2}
set myCounter to (count text items of myString1) - 1
set AppleScript's text item delimiters to oldDelimiters

display dialog myCounter buttons ("OK") default button 1
```

### Das erste Zeichen eines Strings ermitteln - Variante 1

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
first character of myString
-- Ergebnis: "M"
```

### Das erste Zeichen eines Strings ermitteln - Variante 2

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
character 1 of myString
-- Ergebnis: "M"
```

### Das mittlere Zeichen eines Strings ermitteln

```applescript
set myString to "ABC"
middle character of myString
-- Ergebnis: "B"
```

### Das letzte Zeichen eines Strings ermitteln - Variante 1

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
last character of myString
-- Ergebnis: "."
```

### Das letzte Zeichen eines Strings ermitteln - Variante 2

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
character -1 of myString
-- Ergebnis: "."
```

### Die Zeichen 5 bis 11 eines Strings ermitteln

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
text 5 through 11 of myString
-- Ergebnis: "DevEdge"
```

### Die Zeichen von Position 15 bis zum Ende des Strings ermitteln - Variante 1

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
text 15 through end of myString
-- Ergebnis: "Einfach mal weiterdenken."
```

### Die Zeichen von Position 15 bis zum Ende des Strings ermitteln - Variante 2

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
text 15 through -1 of myString
-- Ergebnis: "Einfach mal weiterdenken."
```

### Die Zeichen von Position 33 bis zum Ende des Strings ermitteln - als Liste

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
characters 33 through -1 of myString
-- Ergebnis: {"d", "e", "n", "k", "e", "n", "."}
```

### Die letzten 10 Zeichen eines Strings ermitteln

```applescript
set myString1 to "Mac DevEdge - Einfach mal weiterdenken."

try
  set myString2 to text -10 thru -1 of myString1
on error
  set myString2 to myString1
end try

return myString2
-- Ergebnis: "terdenken."
```

### Ein zufälliges Zeichen eines Strings ermitteln

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
some character of myString
-- Ergebnis: "h" oder "g" oder "w" ...
```

### Einen String umkehren

```applescript
set myString to "Mac DevEdge - Einfach mal weiterdenken."
reverse of characters of myString as text
-- Ergebnis: ".neknedretiew lam hcafniE - egdEveD caM"
```
