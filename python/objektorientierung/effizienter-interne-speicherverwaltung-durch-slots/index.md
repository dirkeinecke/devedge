---
title: Effizienter interne Speicherverwaltung durch Slots
---

## Effizienter interne Speicherverwaltung durch Slots

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):

  __slots__ = ("vorname", "nachname", "geburtsjahr")

  def __init__(self, vorname, nachname, geburtsjahr):
    self.vorname = vorname
    self.nachname = nachname
    self.geburtsjahr = geburtsjahr

  def __del__(self):
    pass

p = Person("Max", "Mustermann", 1979)
```
