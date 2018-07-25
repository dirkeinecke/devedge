---
title: Teilzeichenkette ersetzen (Python)
---

## Teilzeichenkette ersetzen (Python)

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.replace("ein", "kein") # Ausgabe: Das ist kein Text.
```

### Beispiel #2 - Anzahl der Ersetungen begrenzen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text. Das ist ein Text."

print s.replace("ein", "kein", 1) # Ausgabe: Das ist kein Text. Das ist ein Text.
```
