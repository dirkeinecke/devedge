---
title: Zeichenketten trennen (Python)
---

## Zeichenketten trennen (Python)

### Beispiel #1 - ohne angegebenes Trennzeichen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.split() # Ausgabe: ['Das', 'ist', 'ein', 'Text.']
```

### Beipsiel #2 - mit angegebenen Trennzeichen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das-ist-ein-Text."

print s.split("-") # Ausgabe: ['Das', 'ist', 'ein', 'Text.']
```

### Beispiel #3 - vom Ende beginnen mit maximaler Anzahl der Trennungen (hier: 2)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist ein Text."

print s.rsplit(" ", 2) # Ausgabe: ['Das', 'ist', 'ein', 'Text.']
```

### Beispiel #4 - Zeilen trennen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Unix\nWindows\r\nMac\rRest"

print s.splitlines() # Ausgabe: ['Unix', 'Windows', 'Mac', 'Rest']
```

### Beispiel #5 - am ersten Vorkommen des Trennzeichens trennen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist der erste Satz. Das ist der zweite Satz."

print s.partition(".") # Ausgabe: ('Das ist der erste Satz', '.', ' Das ist der zweite Satz.')
```

### Beispiel #6 - am letzten Vorkommen des Trennzeichens trennen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das ist der erste Satz. Das ist der zweite Satz."

print s.rpartition(".") # Ausgabe: ('Das ist der erste Satz. Das ist der zweite Satz', '.', '')
```
