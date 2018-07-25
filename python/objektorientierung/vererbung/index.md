---
title: Vererbung
---

## Vererbung

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Zaehler(object):
  Anzahl = 0
    
  def __init__(self):
    type(self).Anzahl += 1
    
  def __del__(self):
    type(self).Anzahl -= 1

class Person(Zaehler):
  def __init__(self, vorname, nachname, geburtsjahr):

    Zaehler.__init__(self)

    self.vorname = vorname
    self.nachname = nachname
    self.geburtsjahr = geburtsjahr
        
  def __del__(self):
    pass

p1 = Person("Max", "Mustermann", 1979)
p2 = Person("Susi", "Sorglos", 1998)

print Person.Anzahl # Ausgabe: 2
```
