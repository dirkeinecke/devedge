---
title: Zeichen am Anfang und Ende entfernen
---

## Zeichen am Anfang und Ende entfernen

### Beispiel #1 - Zeichen am Anfang und Ende entfernen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "  Das ist ein Text.  "

print s.strip() # Ausgabe: Das ist ein Text.
```

### Beispiel #2 - Zeichen am Anfang entfernen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "  Das ist ein Text.  "

print s.lstrip() # Ausgabe: Das ist ein Text.  
```

### Beispiel #3 - Zeichen am Ende entfernen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

print "Content-type: text/plain\n\n"

s = "  Das ist ein Text.  "

print s.rstrip() # Ausgabe:   Das ist ein Text.
```
