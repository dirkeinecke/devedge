---
title: Docstrings (Documentation Strings)
---

## Docstrings (Documentation Strings)

### Beispiel #1 - Klasse

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

class foo(object):
  """
  Dieser Platz kann genutzt werden um zu beschreiben,
  was die Klasse macht.
  """
  pass

print foo.__doc__

# Ausgabe:
#
#  Dieser Platz kann genutzt werden um zu beschreiben,
#  was die Klasse macht.
```

### Beispiel #2 - Funktion

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

def foo():
  """
  Dieser Platz kann genutzt werden um zu beschreiben,
  was die Funktion macht.
  """
  pass

print foo.__doc__

# Ausgabe:
#
#  Dieser Platz kann genutzt werden um zu beschreiben,
#  was die Funktion macht.
```
