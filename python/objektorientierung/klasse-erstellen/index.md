---
title: Klasse erstellen
---

## Klasse erstellen

### Beispiel #1 - leere Klasse

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  pass
```

### Beispiel #2 - Konstruktor

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  def __init__(self):
    pass

Person()
```

### Beispiel #3 - Konstruktor und Destruktor

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  def __init__(self):
    pass
  def __del__(self):
    pass

obj = Person()
del obj
```

### Beispiel #4 - alle Attribute dem Konstruktor hinzufügen

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

p = Person("Max", "Mustermann", 1979)

print p.vorname # Ausgabe: Max
print p.nachname # Ausgabe: Mustermann
print p.geburtsjahr # Ausgabe: 1979

del p
```

### Beispiel #5 - Attribute als privat (mit "__" vor dem Namen) kennzeichnen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  def __init__(self, vorname, nachname, geburtsjahr):
    self.__vorname = vorname
    self.__nachname = nachname
    self.__geburtsjahr = geburtsjahr
  def __del__(self):
    pass

p = Person("Max", "Mustermann", 1979)

print p.__vorname

del p
```

Durch den Zugriffsversuch auf das private Attribut `__vorname` wird folgender Fehler verursacht:

```
Traceback (most recent call last):
  File "Objektorientierung.py", line 16, in 
    print p.__vorname
AttributeError: 'Person' object has no attribute '__vorname'
```

### Beispiel #6 - Zugriff auf private Attribute über Getter-Methoden

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  def __init__(self, vorname, nachname, geburtsjahr):
    self.__vorname = vorname
    self.__nachname = nachname
    self.__geburtsjahr = geburtsjahr

  def __del__(self):
    pass

  def getVorname(self):
    return self.__vorname

  def getNachname(self):
    return self.__nachname

  def getGeburtsjahr(self):
    return self.__geburtsjahr

p = Person("Max", "Mustermann", 1979)

print p.getVorname() # Ausgabe: Max
print p.getNachname() # Ausgabe: Mustermann
print p.getGeburtsjahr() # Ausgabe: 1979

del p
```

### Beispiel #7 - Zugriff auf private Attribute über Setter-Methoden

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  def __init__(self, vorname, nachname, geburtsjahr):
    self.__vorname = vorname
    self.__nachname = nachname
    self.__geburtsjahr = geburtsjahr

  def __del__(self):
    pass

  def getVorname(self):
    return self.__vorname

  def getNachname(self):
    return self.__nachname

  def getGeburtsjahr(self):
    return self.__geburtsjahr

  def setVorname(self, neuerVorname):
    if type(neuerVorname) is str and neuerVorname != "":
      self.__vorname = neuerVorname
      return True
    else:
      return False

  def setNachname(self, neuerNachname):
    if type(neuerNachname) is str and neuerNachname != "":
      self.__nachname = neuerNachname
      return True
    else:
      return False

  def setGeburtsjahr(self, neuesGeburtsjahr):
    if type(neuesGeburtsjahr) is int:
      self.__geburtsjahr = neuesGeburtsjahr
      return True
    else:
      return False

p = Person("Max", "Mustermann", 1979)

print p.getVorname() # Ausgabe: Max
print p.getNachname() # Ausgabe: Mustermann
print p.getGeburtsjahr() # Ausgabe: 1979

p.setVorname("Susi")
p.setNachname("Sorglos")
p.setGeburtsjahr(1998)

print p.getVorname() # Ausgabe: Susi
print p.getNachname() # Ausgabe: Sorglos
print p.getGeburtsjahr() # Ausgabe: 1998

del p
```

### Beispiel #8 - Managed Attributes (verwaltete Attribute)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  def __init__(self, vorname, nachname, geburtsjahr):
    self.__vorname = vorname
    self.__nachname = nachname
    self.__geburtsjahr = geburtsjahr

  def __del__(self):
    pass

  def getVorname(self):
    return self.__vorname

  def getNachname(self):
    return self.__nachname

  def getGeburtsjahr(self):
    return self.__geburtsjahr

  def setVorname(self, neuerVorname):
    if type(neuerVorname) is str and neuerVorname != "":
      self.__vorname = neuerVorname

  def setNachname(self, neuerNachname):
    if type(neuerNachname) is str and neuerNachname != "":
      self.__nachname = neuerNachname

  def setGeburtsjahr(self, neuesGeburtsjahr):
    if type(neuesGeburtsjahr) is int:
      self.__geburtsjahr = neuesGeburtsjahr

  # Managed Attributes (verwaltete Attribute)
  vorname = property(getVorname, setVorname)
  nachname = property(getNachname, setNachname)
  geburtsjahr = property(getGeburtsjahr, setGeburtsjahr)

p = Person("Max", "Mustermann", 1979)

print p.vorname # Ausgabe: Max
print p.nachname # Ausgabe: Mustermann
print p.geburtsjahr # Ausgabe: 1979

p.vorname = "Susi"
p.nachname = "Sorglos"
p.geburtsjahr = 1998

print p.vorname # Ausgabe: Susi
print p.nachname # Ausgabe: Sorglos
print p.geburtsjahr # Ausgabe: 1998

del p
```

### Beispiel #9 - Klassen-Attribute (class members) - hier: anzahl

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class Person(object):
  anzahl = 0

  def __init__(self, vorname, nachname, geburtsjahr):
    self.vorname = vorname
    self.nachname = nachname
    self.geburtsjahr = geburtsjahr
    Person.anzahl += 1

  def __del__(self):
    Person.anzahl -= 1

p1 = Person("Max", "Mustermann", 1979)
p2 = Person("Susi", "Sorglos", 1998)

print Person.anzahl # Ausgabe: 2

del p1

print Person.anzahl # Ausgabe: 1

del p2

print Person.anzahl # Ausgabe: 0
```
