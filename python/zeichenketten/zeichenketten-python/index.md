---
title: Zeichenketten (Python)
---

## Zeichenketten (Python)

### Beispiel #1 - Zeichenkette definieren und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s # Ausgabe: Das ist ein Text.
```

### Beispiel #2 - Zeichenkette über mehrere Zeilen definieren und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = """Das ist
ein Text."""

print s

"""
Ausgabe:

Das ist
ein Text.

"""
```

### Beispiel #3

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

if "ist" in s:
  print "Enthalten"
else:
  print "Nicht enthalten"

# Ausgabe: Enthalten
```

### Beispiel #4

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

if "foo" not in s:
  print "Nicht enthalten"
else:
  print "Enthalten"

# Ausgabe: Nicht enthalten
```

### Beispiel #5 - Zeichenketten verknüpfen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

vorname = "Max"
nachname = "Mustermann"

name = vorname + " " + nachname

print name # Ausgabe: Max Mustermann
```

### Beispiel #6 - Zeichenketten verknüpfen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

name = "Max"
name += " Mustermann"

print name # Ausgabe: Max Mustermann
```

### Beispiel #7 - Zeichenketten verknüpfen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist" " " "ein Text."

print s # Ausgabe: Das ist ein Text.
```

### Beispiel #8 - Zeichenketten wiederholen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = 3 * "Tor! "

print s # Ausgabe: Tor! Tor! Tor!
```

### Beispiel #9 - Zeichenketten wiederholen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Tor! " * 3

print s # Ausgabe: Tor! Tor! Tor!
```

### Beispiel #10 - Zugriff auf bestimmte Elemente (positiver Index)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "ABC"

print s[2] # Ausgabe: C
```

### Beispiel #11 - Zugriff auf bestimmte Elemente (negativer Index)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s[-3] # Ausgabe: x
```

### Beispiel #12 - Teilzeichenkette (Start:Stop)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s[4:7] # Ausgabe: ist
```

### Beispiel #13 - Teilzeichenkette (Start:Stop)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s[4:-10] # Ausgabe: ist
```

Indizes können weggelassen werden.

### Beispiel #14 - Teilzeichenkette (Start:Stop)

Wird der erste Index weggelassen, dann wird das erste Element angenommen.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s[4:] # Ausgabe: ist ein Text.
```

### Beispiel #15 - Teilzeichenkette (Start:Stop)

Wird der zweite Index weggelassen, dann wird das letzte Element angenommen.

```
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s[:7] # Ausgabe: Das ist
```

### Beispiel #16 - Kopie einer Zeichenkette ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s[:] # Ausgabe: Das ist ein Text.
```

### Beispiel #17 - Teilzeichenkette (Start:Stop:Step)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "0123456789"

print s[1:10:2] # Ausgabe: 13579
```

### Beispiel #18 - Zeichenkette umdrehen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "Das ist ein Text."

print s[::-1] # Ausgabe: .txeT nie tsi saD
```

### Beispiel #19 - kleinste Element

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "zeichenkette"

print min(s) # Ausgabe: c
```

### Beispiel #20 - größte Element

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

s = "zeichenkette"

print max(s) # Ausgabe: z
```
