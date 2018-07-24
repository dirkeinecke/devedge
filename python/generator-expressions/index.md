---
title: Generator Expressions
---

## Generator Expressions

Generator Expressions erzeugen keine Liste wie die List Comprehensions.

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

g = sum( (x * 10 for x in range(10)) )
print g # Ausgabe: 450
```
