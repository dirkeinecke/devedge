---
title: Rekursive Funktionen
---

## Rekursive Funktionen

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def summe(zahl):
  if zahl < 10:
    return summe(zahl + 1)
  else:
    return zahl

print summe(0) # Ausgabe: 10
```
