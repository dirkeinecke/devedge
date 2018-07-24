---
title: Datei schreiben
---

## Datei schreiben

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

fobj = open("ausgabe.txt", "w")

fobj.write("Zeile 1\n")
fobj.write("Zeile 2\n")
fobj.write("Zeile 3")

fobj.close()
```

### Beispiel #2

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

fobj = open("ausgabe.txt", "w")

print >> fobj, "Zeile 1"
print >> fobj, "Zeile 2"
print >> fobj, "Zeile 3",

fobj.close()
```
