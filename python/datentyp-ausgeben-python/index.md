---
title: Datentyp ausgeben (Python)
---

## Datentyp ausgeben (Python)

### Beispiel #1 - Integer

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

print type(123) # Ausgabe: <type 'int'>
```

### Beispiel #2 - String

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

print type("ABC") # Ausgabe: <type 'str'>
```

### Beispiel #3

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

if type(123) == int:
  print "Integer"
else:
  print "Kein Integer"
```

### Beispiel #4

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

if type("ABC") == str:
  print "String"
else:
  print "String"
```
