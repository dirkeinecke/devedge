---
title: Datei einlesen
---

## Datei einlesen

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

fobj = open("testdatei.txt", "r")

for line in fobj:
  print line

fobj.close()
```

### Beispiel #2 - Datei einlesen und Inhalt in Dictionary speichern

Inhalt der Datei "namen.txt":

```
Max Mustermann
Erika Mustermann
Felix Muster
Maria Müller
John Doe
Jan Janssen
Susi Sorglos
```

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

namen = {}

fobj = open("namen.txt", "r")

for line in fobj:
  line = line.strip()
  name = line.split(" ")
  namen[name[0]] = name[1]

fobj.close()

print namen

# Ausgabe:
# {'Susi': 'Sorglos', 'Max': 'Mustermann', 'Felix': 'Muster', 'Jan': 'Janssen', 'Erika': 'Mustermann', 'John': 'Doe', 'Maria': 'M\xc3\xbcller'}
```
