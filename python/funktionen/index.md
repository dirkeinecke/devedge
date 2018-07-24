---
title: Funktionen
---

## Funktionen

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def summe(zahl):
  zahl = zahl + 1
  return zahl

print summe(1) # Ausgabe: 2
```

### Beispiel #2 - Funktion vorzeitig abbrechen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def summe(zahl):
  if type(zahl) != int:
    return None
  else:
    zahl = zahl + 1
    return zahl

ergebnis = summe("abc")

if ergebnis is None:
  print "Keine Ganzzahl angegeben." # Ausgabe
else:
  print ergebnis
```

### Beispiel #3 - Funktion als Instanz behandeln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def summe(zahl):
  zahl = zahl + 1
  return zahl

summe_bilden = summe

print summe_bilden(1) # Ausgabe: 2
```

### Beispiel #4 - optionale Parameter

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def summe(a, b, c=0, d=0):
  return a + b + c + d

print summe(1, 2) # Ausgabe: 3
print summe(1, 2, 4) # Ausgabe: 7
print summe(1, 2, 4, 13) # Ausgabe: 20
```

### Beispiel # 4 - keyword arguments

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def summe(a, b, c=0, d=0):
  return a + b + c + d

print summe(a=1, b=2) # Ausgabe: 3
print summe(a=1, b=2, d=4) # Ausgabe: 7
print summe(a=1, b=2, d=4, c=13) # Ausgabe: 20
```
