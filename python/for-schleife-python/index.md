---
title: for-Schleife (Python)
---

## for-Schleife (Python)

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

for i in range(5): # stop
  print i

# Ausgabe: 0 1 2 3 4
```

### Beispiel #2

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

for i in range(10, 20): # start, stop
  print i

# Ausgabe: 10 11 12 13 14 15 16 17 18 19
```

### Beispiel #3

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

for i in range(0, 10, 2): # start, stop, step
  print i

# Ausgabe: 0 2 4 6 8
```

### Beispiel #4

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

for i in range(10, 0, -2): # start, stop, step
  print i

# Ausgabe: 10 8 6 4 2
```

### Beispiel #5

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

for c in "Hallo Welt":
  print c

"""
Ausgabe:

H
a
l
l
o
 
W
e
l
t

"""
```

### Beispiel #6

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

for c in "Hallo Welt":
  print c
else:
  print "Hallo Welt"


"""
Ausgabe:

H
a
l
l
o
 
W
e
l
t
Hallo Welt

"""
```
