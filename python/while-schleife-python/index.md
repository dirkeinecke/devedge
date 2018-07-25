---
title: while-Schleife (Python)
---

## while-Schleife (Python)

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 0

while x < 10:
  print x
  x = x + 1
```

### Beispiel #2

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 0

while x < 10:
  print x
  x = x + 1
else: # Wenn die Bedingung das erste mal False ergibt
  print "Fertig!"
```

### Beispiel #3 - vorzeitiger Abbruch der Schleife

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 0

while x < 10:
  if x == 5:
    print "Schleife bei x == 5 abgebrochen"
    break
  print x
  x = x + 1
else: # Wenn die Bedingung das erste mal False ergibt
  print "Fertig!"
```

### Beispiel #4 - vorzeitiger Abbruch eines Schleifendurchlaufs

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

x = 0

while x < 10:
  if x == 5:
    print "x == 5 überspringen"
    x = x + 1
    continue
  print x
  x = x + 1
else: # Wenn die Bedingung das erste mal False ergibt
  print "Fertig!"
```
