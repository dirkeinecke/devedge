---
title: Listen (Python)
---

## Listen (Python)

### Beispiel #1 - Liste definieren und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = [1, 0.5, "Hallo Welt", 2]

print l # Ausgabe: [1, 0.5, 'Hallo Welt', 2]
```

### Beispiel #2 - auf einzelne Elemente zugreifen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = [1, 0.5, "Hallo Welt", 2]

print l[1] # Ausgabe: 0.5
```

### Beispiel #3 - Werte einzelner Elemente ändern

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = [1, 0.5, "Hallo Welt", 2]

l[3] = "foo bar"

print l # Ausgabe: [1, 0.5, 'Hallo Welt', 'foo bar']
```

### Beispiel #4 - einzelne Elemente entfernen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = [1, 0.5, "Hallo Welt", 2]

del l[3]

print l # Ausgabe: [1, 0.5, 'Hallo Welt']
```

### Beispiel #5 - mehrere Elemente entfernen (Start:Stop)

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = [1, 0.5, "Hallo Welt", 2, "foo bar", 10]

del l[2:4]

print l # Ausgabe: [1, 0.5, 'foo bar', 10]
```

### Beispiel #6 - Ersetzen von Teillisten

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]

l[2:4] = ["c", "d"]

print l # Ausgabe: ['A', 'B', 'c', 'd', 'E', 'F', 'G']
```

### Beispiel #7 - Einfügen neuer Elemente

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]

l[2:4] = ["c", "d", 1, 2, 3]

print l # Ausgabe: ['A', 'B', 'c', 'd', 1, 2, 3, 'E', 'F', 'G']
```

### Beispiel #8 - ein Element am Ende hinzufügen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]
l.append("H")

print l # Ausgabe: ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H']
```

### Beispiel #9 - Liste ans Ende einer Liste anhängen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l1 = ["A", "B", "C", "D", "E", "F", "G"]
l2 = [1, 2, 3]

l1.extend(l2)

print l1 # Ausgabe: ['A', 'B', 'C', 'D', 'E', 'F', 'G', 1, 2, 3]
```

### Beispiel #10 - Anzahl der Vorkommen eines Elements ermitteln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "A", "C", "A", "E", "F", "A"]

print l.count("A") # Ausgabe: 4
```

### Beispiel #11 - Index des ersten Vorkommens eines Elements ermitteln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]

print l.index("C") # Ausgabe: 2
```

### Beispiel #12 - Element an einer bestimmten Position einfügen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "D", "E", "F", "G"]

l.insert(2, "C") # Index, Element

print l # Ausgabe: ['A', 'B', 'C', 'D', 'E', 'F', 'G']
```

### Beispiel #13 - letztes Element entfernen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]

l.pop()

print l # Ausgabe: ['A', 'B', 'C', 'D', 'E', 'F']
```

### Beispiel #14 - Element mit einem bestimmten Index entfernen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]

l.pop(2)

print l # Ausgabe: ['A', 'B', 'D', 'E', 'F', 'G']
```

### Beispiel #15 - erstes Vorkommen eines bestimmten Elements entfernen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]

l.remove("C")

print l # Ausgabe: ['A', 'B', 'D', 'E', 'F', 'G']
```

### Beispiel #16 - Reihenfolge umkehren

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = ["A", "B", "C", "D", "E", "F", "G"]

l.reverse()

print l # Ausgabe: ['G', 'F', 'E', 'D', 'C', 'B', 'A']
```

### Beispiel #17 - Elemente sortieren

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = [3, 6, 8, 5, 0, 1, 7, 2, 4, 9]

l.sort()

print l # Ausgabe: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

### Beispiel #18 - Elemente in umgekehrter Reihenfolge sortieren

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/html\n\n"

l = [3, 6, 8, 5, 0, 1, 7, 2, 4, 9]

l.sort(reverse = True)

print l # Ausgabe: [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
```

### Beispiel #19 - Anzahl der Elemente ermitteln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

liste = [1, 2, 3, 4, 5, 6, 7, 8, 9]

print len(liste) # Ausgabe: 9
```

### Beispiel #20 - zufälliges Element ermitteln

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import random

print "Content-type: text/plain\n\n"

l = [1, 0.5, "Hallo Welt", 2]

random.seed()
print random.choice(l) # Ausgabe zum Beispiel: Hallo Welt
```

### Beispiel #21 - Liste einer bestimmten Anzahl (hier: 3) zufälliger Elemente einer Liste erzeugen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import random

print "Content-type: text/plain\n\n"

l = [1, 2, 3, 4, 5]

random.seed()
print random.sample(l, 3) # Ausgabe zum Beispiel: [2, 5, 3]
```

### Beispiel #22 - Liste in zufällige Reihenfolge bringen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import random

print "Content-type: text/plain\n\n"

l = [1, 2, 3, 4, 5]

random.seed()
random.shuffle(l)
print l # Ausgabe zum Beispiel: [5, 3, 2, 1, 4]
```
