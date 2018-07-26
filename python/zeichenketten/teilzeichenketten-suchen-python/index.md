---
title: Teilzeichenketten suchen (Python)
---

## Teilzeichenketten suchen (Python)

### Beispiel #1 A - Index des ersten Vorkommens ermitteln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.find("e") # Ausgabe: 8
```

### Beispiel #1 B - Index des ersten Vorkommens ermitteln

Wird die zu suchende Teilzeichenkette nicht gefunden, wird ein `ValueError` erzeugt.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.index("e") # Ausgabe: 8
```

### Beispiel #2 A - Index des letzten Vorkommens ermitteln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.rfind("e") # Ausgabe: 13
```

### Beispiel #2 B - Index des letzten Vorkommens ermitteln

Wird die zu suchende Teilzeichenkette nicht gefunden, wird ein `ValueError` erzeugt.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.rindex("e") # Ausgabe: 13
```

### Beispiel #3 - Anzahl der Vorkommen einer Teilzeichenkette ermitteln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.count("e") # Ausgabe: 2
```
