---
title: Generatoren
---

## Generatoren

### Beispiel #1 - schlechte Performance

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

for i in range(10):
  print i, # Ausgabe: 0 1 2 3 4 5 6 7 8 9
```

### Beispiel #2 - gute Performance durch Einsatz des Generators xrange()

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

for i in xrange(10):
  print i, # Ausgabe: 0 1 2 3 4 5 6 7 8 9
```
