---
title: Zeichenketten testen
---

## Zeichenketten testen

### Beispiel #1 - alles Buchstaben oder alles Zahlen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "ABC"

if s.isalnum() == True:
  print "Alles Buchstaben oder Ziffern" # Ausgabe
else:
  print "Buchstaben und Ziffern und ... gemischt"
```

### Beispiel #2 - alles Buchstaben oder alles Zahlen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "123"

if s.isalnum() == True:
  print "Alles Buchstaben oder Ziffern" # Ausgabe
else:
  print "Buchstaben und Ziffern und ... gemischt"
```

### Beispiel #3 - alles Buchstaben oder alles Zahlen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "ABC 123"

if s.isalnum() == True:
  print "Alles Buchstaben oder Ziffern"
else:
  print "Buchstaben und Ziffern und ... gemischt" # Ausgabe
```

### Beispiel #4 - alles Buchstaben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "ABC"

if s.isalpha() == True:
  print "Alles Buchstaben" # Ausgabe
else:
  print "nicht alles Buchstaben"
```

### Beispiel #5 - alles Zahlen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "123"

if s.isdigit() == True:
  print "Alles Zahlen" # Ausgabe
else:
  print "nicht alles Zahlen"
```

### Beispiel #6 - alles Kleinbuchstaben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "das ist ein text."

if s.islower() == True:
  print "alles Kleinbuchstaben" # Ausgabe
else:
  print "nicht alles Kleinbuchstaben"
```

### Beipsiel #7 - alles Großbuchstaben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "DAS IST EIN TEXT."

if s.isupper() == True:
  print "alles Großbuchstaben" # Ausgabe
else:
  print "nicht alles Großbuchstaben"
```

### Beispiel #8 - alles Whitespaces

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = " \n \t "

if s.isspace() == True:
  print "alles Whitespaces" # Ausgabe
else:
  print "nicht alles Whitespaces"
```

### Beispiel #9 - alle Anfangsbuchstaben groß geschrieben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "Das Ist Ein Text."

if s.istitle() == True:
  print "alle Anfangsbuchstaben groß" # Ausgabe
else:
  print "nicht alle Anfangsbuchstaben groß"
```
