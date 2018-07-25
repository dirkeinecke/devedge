---
title: XML-Datei erzeugen
---

## XML-Datei erzeugen

### Beispiel #1 - Python-Datei

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import xml.dom.minidom as dom

print "Content-type: text/plain\n\n"

baum = dom.Document()
tag_personen = dom.Element("personen")
tag_person = dom.Element("person")
tag_person.setAttribute("id", "1")
tag_vorname = dom.Element("vorname")
text = dom.Text()
text.data = "Max"
tag_vorname.appendChild(text)
tag_nachname = dom.Element("nachname")
text = dom.Text()
text.data = "Mustermann"
tag_nachname.appendChild(text) 
tag_person.appendChild(tag_vorname)
tag_person.appendChild(tag_nachname)
tag_personen.appendChild(tag_person)
baum.appendChild(tag_personen)

f = open("Personen.xml", "w")
baum.writexml(f, "", "\t", "\n")
f.close()
```

### Beispiel #1 - erzeugte XML-Datei

```xml
<?xml version="1.0" ?>
<personen>
  <person id="1">
    <vorname>
      Max
    </vorname>
    <nachname>
      Mustermann
    </nachname>
  </person>
</personen>
```
