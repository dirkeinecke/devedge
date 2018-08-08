---
title: Datensätze (records)
---

## Datensätze (records)

Die folgenden Beispiele zeigen dem Umgang mit Datensätzen (records). Beachten Sie dabei immer, dass Records in Anführungszeichen (`""`) eingeschlossen sein müssen.

### Einen Datensatz (record) mit zwei Name/Wert-Paaren definieren

```applescript
set myRecord to {Site:"Mac DevEdge", Claim:"Einfach mal weiterdenken."}
-- Ergebnis: {name:"Mac DevEdge", Claim:"Einfach mal weiterdenken."}
```

### Testen ob der Inhalt einer Variablen ein Datensatz (record) ist

```applescript
set myRecord to {Site:"Mac DevEdge", Claim:"Einfach mal weiterdenken."}
if class of myRecord is record then
  display dialog "Ist ein Datensatz (record)" buttons ("OK") default button 1
else
  display dialog "Ist kein Datensatz (record)" buttons ("OK") default button 1
end if
```

### Einen Datensatz (record) mit Name/Wert-Paaren bestehend aus Strings und Zahlen definieren

```applescript
set myRecord to {Value1:"Mac DevEdge", Value2:"Einfach mal weiterdenken.", Value3:10, Value4:23.5}
-- Ergebnis: {Value1:"Mac DevEdge", Value2:"Einfach mal weiterdenken.", Value3:10, Value4:23.5}
```

### Einen Datensatz (record) mit Name/Wert-Paaren bestehend aus einem Variablenwert (string), einem String und Zahlen definieren

```applescript
set myString to "Mac DevEdge"
set myRecord to {Value1:myString, Value2:"Ein String", Value3:10, Value4:23.5}
-- Ergebnis: {Value1:"Mac DevEdge", Value2:"Ein String", Value3:10, Value4:23.5}
```

### Einen Datensatz (record) aus zwei Datensätzen (records) definieren

```applescript
set myRecord1 to {Value1:"Mac", Value2:"DevEdge"}
set myRecord2 to {Value1:10, Value2:20, Value3:30}
set myRecord to {Record1:myRecord1, Record2:myRecord2}
-- Ergebnis:
-- {Record1:{Value1:"Mac", Value2:"DevEdge"}, Record2:{Value1:10, Value2:20, Value3:30}}
```

### Zwei Datensätze (records) kombinieren

```applescript
set myRecord1 to {Value1:"Mac", Value2:"DevEdge"}
set myRecord2 to {Value1:10, Value2:20, Value3:30}
set myRecord to myRecord1 & myRecord2
-- Ergebnis: {Value1:"Mac", Value2:"DevEdge", Value3:30}

set myRecord1 to {Value1:"Mac", Value2:"DevEdge"}
set myRecord2 to {Value3:10, Value4:20, Value5:30}
set myRecord to myRecord1 & myRecord2
-- Ergebnis: {Value1:"Mac", Value2:"DevEdge", Value3:10, Value4:20, Value5:30}
```

### Den Wert einer Eigenschaft (Name/Wert-Paar) eines Datensatzes (record) ändern

```applescript
set myRecord to {Value1:"Mac", Value2:"DevEdge"}
set Value2 of myRecord to "DevEdge - Einfach mal weiterdenken."
get myRecord
-- Ergebnis: {Value1:"Mac", Value2:"DevEdge - Einfach mal weiterdenken."}
```

### Anzahl der Eigenschaften (Name/Wert-Paare) eines Datensatzes (record) zählen - Variante 1

```applescript
set myRecord to {Value1:"Mac", Value2:"DevEdge"}
set myQuantity to the length of myRecord
-- Ergebnis: 2
```

### Anzahl der Eigenschaften (Name/Wert-Paare) eines Datensatzes (record) zählen - Variante 2

```applescript
set myRecord to {Value1:"Mac", Value2:"DevEdge"}
set myQuantity to the count of myRecord
-- Ergebnis: 2
```

### Prüfen ob sich eine bestimmte Eigenschaft (Name/Wert-Paar) in einem Datensatz (record) befindet - Variante 1

```applescript
set myRecord to {Value1:10, Value2:20, Value3:30}
if myRecord contains {Value1:10} then
  display dialog "Ist enhalten" buttons ("OK") default button 1 -- trifft zu
else
  display dialog "Ist nicht enthalten" buttons ("OK") default button 1
end if
```

### Prüfen ob sich eine bestimmte Eigenschaft (Name/Wert-Paar) in einem anderen Datensatz (record) befindet - Variante 2

```applescript
set myRecord to {Value1:10, Value2:20, Value3:30}
if {Value1:10} is in myRecord then
  display dialog "Ist enhalten" buttons ("OK") default button 1 -- trifft zu
else
  display dialog "Ist nicht enthalten" buttons ("OK") default button 1
end if
```

### Prüfen ob sich die Eigenschaften (Name/Wert-Paare) eines Datensatzes (record) in einem anderen Datensatz (record) befinden

```applescript
set myRecord to {Value1:10, Value2:20, Value3:30}
if myRecord contains {Value1:10, Value2:20} then
  display dialog "Sind enhalten" buttons ("OK") default button 1 -- trifft zu
else
  display dialog "Sind nicht enthalten" buttons ("OK") default button 1
end if

set myRecord to {Value1:10, Value2:20, Value3:30}
-- Beim Vergleich von Records ist die Reihenfolge egal
if myRecord contains {Value2:20, Value1:10} then
  display dialog "Sind enhalten" buttons ("OK") default button 1 -- trifft zu
else
  display dialog "Sind nicht enthalten" buttons ("OK") default button 1
end if
```
