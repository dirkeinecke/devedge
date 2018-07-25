---
title: Anfang und Ende testen
---

## Anfang und Ende testen

### Beispiel #1 - Anfang

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: utf8\n\n"

s = "Das ist ein Text."

if s.startswith("Das"):
  print "Anfang ist 'Das'" # Ausgabe
else:
  print "Anfang ist nicht 'Das'"
```

### Beispiel #2 - Ende

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: utf8\n\n"

s = "Das ist ein Text."

if s.endswith("."):
  print "Ende ist '.'" # Ausgabe
else:
  print "Ende ist nicht '.'"
```
