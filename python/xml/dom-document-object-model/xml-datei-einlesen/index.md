---
title: XML-Datei einlesen
---

## XML-Datei einlesen

### Beispiel #1 - XML-Datei "Personen.xml"

```xml
<?xml version="1.0" encoding="UTF-8"?>
<personen>
  <person id="1">
    <vorname>Max</vorname>
    <nachname>Mustermann</nachname>
  </person>
  <person id="2">
    <vorname>Susi</vorname>
    <nachname>Sorglos</nachname>
  </person>
</personen>
```

### Beispiel #1 - Python-Datei - Schritt 1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import xml.dom.minidom as dom

print "Content-type: text/plain\n\n"

baum = dom.parse("Personen.xml")

for eintrag in baum.firstChild.childNodes:
  print eintrag.nodeName

"""
Ausgabe:

#text
person
#text
person
#text
"""
```

### Beispiel #1 - Python-Datei - Schritt 2

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import xml.dom.minidom as dom

print "Content-type: text/plain\n\n"

baum = dom.parse("Personen.xml")

for eintrag in baum.firstChild.childNodes:
  if eintrag.nodeName == "person":
    for knoten in eintrag.childNodes:
      print knoten.nodeName

"""
Ausgabe:

#text
vorname
#text
nachname
#text
#text
vorname
#text
nachname
#text
"""
```

### Beispiel #1 - Python-Datei - Schritt 3

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import xml.dom.minidom as dom

print "Content-type: text/plain\n\n"

baum = dom.parse("Personen.xml")

for eintrag in baum.firstChild.childNodes:
  if eintrag.nodeName == "person":
    for knoten in eintrag.childNodes:
      if knoten.nodeName == "vorname":
        print "Vorname: " + knoten.firstChild.data.strip()
      elif knoten.nodeName == "nachname":
        print "Nachname: " + knoten.firstChild.data.strip()

"""
Ausgabe:

Vorname: Max
Nachname: Mustermann
Vorname: Susi
Nachname: Sorglos
"""
```

### Beispiel #1 - Python-Datei - Schritt 4 (Attribute lesen, hier: id)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import xml.dom.minidom as dom

print "Content-type: text/plain\n\n"

baum = dom.parse("Personen.xml")

for eintrag in baum.firstChild.childNodes:
  if eintrag.nodeName == "person":
    print "ID: " + eintrag.getAttribute("id")
    for knoten in eintrag.childNodes:
      if knoten.nodeName == "vorname":
        print "Vorname: " + knoten.firstChild.data.strip()
      elif knoten.nodeName == "nachname":
        print "Nachname: " + knoten.firstChild.data.strip()

"""
Ausgabe:

ID: 1
Vorname: Max
Nachname: Mustermann
ID: 2
Vorname: Susi
Nachname: Sorglos
"""
```
