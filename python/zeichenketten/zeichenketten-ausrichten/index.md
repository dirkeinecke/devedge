---
title: Zeichenketten ausrichten
---

## Zeichenketten ausrichten

### Beispiel #1 - mittig ausrichten

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.center(50, "-") # Ausgabe: ----------------Das ist ein Text.-----------------
```

### Beispiel #2 - links ausrichten

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.ljust(50, "-") # Ausgabe: Das ist ein Text.---------------------------------
```

### Beispiel #3 - rechts ausrichten

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.rjust(50, "-") # Ausgabe: ---------------------------------Das ist ein Text.
```

### Beispiel #4 - Numerische Werte rechts ausrichten und mit Nullen auffüllen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print "23.05".zfill(10) # Ausgabe: 0000023.05
```
