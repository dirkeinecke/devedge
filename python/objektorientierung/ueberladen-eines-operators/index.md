---
title: Überladen eines Operators
---

## Überladen eines Operators

### Beispiel #1 - für den Vergleich mit ==

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):

  def __init__(self, vorname, nachname, geburtsjahr):
    self.vorname = vorname
    self.nachname = nachname
    self.geburtsjahr = geburtsjahr

  def __del__(self):
    pass

  def __eq__(self, anderePerson):
    return self.nachname == anderePerson.nachname

p1 = Person("Max", "Mustermann", 1979)
p2 = Person("Susi", "Sorglos", 1998)

print p1 == p2 # Ausgabe: False
```
