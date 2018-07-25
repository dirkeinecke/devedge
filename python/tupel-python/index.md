---
title: Tupel (Python)
---

## Tupel (Python)

### Beispiel #1 - Tupel definieren und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

t = (1, 2, 3)

print t # Ausgabe: (1, 2, 3)
```

### Beispiel #2 - leeres Tupel definieren und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

t = ()

print t # Ausgabe: ()
```

### Beispiel #3 - Tuple mit nur einem Wert definieren und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

t = (1) # SO NICHT
t = (1,)

print t # Ausgabe: (1,)
```

### Beispiel #4 - auf einzelne Elemente zugreifen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

t = ("A", "B", "C")

print t[1] # Ausgabe: B
```
