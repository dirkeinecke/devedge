---
title: List Comprehensions
---

## List Comprehensions


Mit List Comprehensions kann man für jedes Element einer Liste eine Aktion durchführen und mit den neuen Elementen eine Liste erzeugen.

### Beispiel #1

Jedes Element der Liste liste1 wird mit dem Faktor 10 multiplizert. Die neuen Elemente werden als nue Liste liste2 gespeichert.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

liste1 = [1, 2, 3, 4, 5, 6, 7, 8, 9]

liste2 = [x * 10 for x in liste1]

print liste2 # Ausgabe: [10, 20, 30, 40, 50, 60, 70, 80, 90]
```

### Beispiel #2 - mit Bedingung

Jedes Element der Liste liste1, welches kleiner als "D" ist, wird in Kleinbuchstaben umgewandelt. Die neuen Elemente werden als neue Liste liste2 gespeichert.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

liste1 = ["A", "B", "C", "D", "E", "F"]

liste2 = [s.lower() for s in liste1 if s < "D"]

print liste2 # Ausgabe: ['a', 'b', 'c']
```

### Beispiel #3 - mit zwei Listen

Jedes Element der Liste liste1 wird mit dem Element des selben Indexes aus Liste liste1 multipliziert. Die neuen Elemente werden als nue Liste liste3 gespeichert.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

liste1 = [1, 2, 3, 4, 5, 6, 7, 8, 9]
liste2 = [10, 20, 30, 40, 50, 60, 70, 80, 90]

liste3 = [liste1[i] * liste2[i] for i in range(len(liste1))]

print liste3 # Ausgabe: [10, 40, 90, 160, 250, 360, 490, 640, 810]
```
