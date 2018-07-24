---
title: Eigene Module
---

## Eigene Module

### Beispiel #1 - Modul

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

def summe(x, y):
  return x + y
```

### Beispiel #1 - Programm

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import mathematik

print "Content-type: text/plain\n\n"

print mathematik.summe(1, 5) # Ausgabe: 6
```
