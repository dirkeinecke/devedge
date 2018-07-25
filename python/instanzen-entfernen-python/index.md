---
title: Instanzen entfernen (Python)
---

## Instanzen entfernen (Python)

Instanzen können in Python nicht entfernt werden. Man kann aber die Referenz freigeben. Dadurch wird die Instanz automatisch entfernt und der Speicher wieder freigegeben.

### Beispiel #1 - Referenz freigeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 123

print x

del x # Referenz freigeben ... Instanz wird entfernt
```

### Beispiel #2 - mehrere Referenzen freigeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 123
y = "ABC"
z = "Hallo Welt"

print x
print y
print z

del x, y, z # Referenzen freigeben ... Instanzen werden entfernt
```
