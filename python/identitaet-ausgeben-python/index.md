---
title: Identität ausgeben (Python)
---

## Identität ausgeben (Python)

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

print id(123) # Ausgabe z.B.: 135768680
```

### Beispiel #2

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

print id("Hallo Welt") # Ausgabe z.B.: 698218280
```
