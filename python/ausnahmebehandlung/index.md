--
title: Ausnahmebehandlung
---

## Ausnahmebehandlung

### Beispiel #1 - IndexError wird behandelt

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def getItem(liste, i):
  try:
    return liste[i]
  except IndexError:
    return "Es existiert kein Element mit dem Index " + str(i) + "."

liste = [1, 2, 3]

print getItem(liste, 5) # Ausgabe: Es existiert kein Element mit dem Index 5.
```

### Beispiel #2 - IndexError und TypeError werden getrennt behandelt

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def getItem(liste, i):
  try:
    return liste[i]
  except IndexError:
    return "Es existiert kein Element mit dem Index " + str(i) + "."
  except TypeError:
    return "Der Index muss ein Integer-Wer sein."

liste = [1, 2, 3]

print getItem(liste, "foo") # Ausgabe: Der Index muss ein Integer-Wer sein.
```

### Beispiel #3 - IndexError und TypeError werden zusammen behandelt

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def getItem(liste, i):
  try:
    return liste[i]
  except (IndexError, TypeError):
    return "Der angegebene Index ist nicht vorhanden oder kein Integer-Wert."

liste = [1, 2, 3]

print getItem(liste, 5) # Ausgabe: Der angegebene Index ist nicht vorhanden oder kein Integer-Wert.
print getItem(liste, "foo") # Ausgabe: Der angegebene Index ist nicht vorhanden oder kein Integer-Wert.
```

### Beispiel #4 - IndexError und TypeError werden zusammen behandelt / Fehlermeldung des Systems ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def getItem(liste, i):
  try:
    return liste[i]
  except (IndexError, TypeError), e:
    return "Fehlermeldung: " + e.message

liste = [1, 2, 3]

print getItem(liste, 5) # Ausgabe: Fehlermeldung: list index out of range
print getItem(liste, "foo") # Ausgabe: Fehlermeldung: list indices must be integers
```

### Beispiel #5

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def getItem(liste, i):
  try:
    print liste[i]
  except (IndexError, TypeError), e:
    print "Fehlermeldung: " + e.message
  else:
    print "Es ist kein Fehler aufgetreten."
  finally:
    print "Diese zeile wird immer ausgegeben."

liste = [1, 2, 3]

getItem(liste, 1)

"""
Ausgabe:

2
Es ist kein Fehler aufgetreten.
Diese zeile wird immer ausgegeben.

"""
```
