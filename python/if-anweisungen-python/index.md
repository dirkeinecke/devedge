---
title: if-Anweisungen (Python)
---

## if-Anweisungen (Python)

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

if 2 == 2:
  print "2 ist gleich 2"
```

### Beispiel #2

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

if 2 == 2 and "foo" != "bar":
  print "2 ist gleich 2 und foo ist nicht bar"
```

### Beispiel #3

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 1

if x == 1: # True
  print "x ist gleich 1"
elif x == 2: # False
  print "x ist gleich 2"
```

### Beispiel #4

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 1

if x == 1: # True
  print "x ist gleich 1"
else:
  print "x ist nicht 1"
```
