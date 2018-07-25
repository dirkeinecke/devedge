---
title: Reguläre Ausdrücke
---

## Reguläre Ausdrücke

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import re

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

if re.search(r"ein", text): # sucht "ein"
  print "Gefunden!"
else:
  print "Nicht gefunden!"
```

### Beispiel #2

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import re

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

if re.search(r"Text.$", text): # sucht "Text." am Ende ($)
  print "Gefunden!"
else:
  print "Nicht gefunden!"
```

### Beispiel #3

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import re

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

if re.search(r"IsT", text, re.I): # sucht "IsT" unabhängig von Klein- und Großschreibung (re.I / re.IGNORECASE)
  print "Gefunden!"
else:
  print "Nicht gefunden!"
```

### Beispiel #3 A

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import re

print "Content-type: text/plain\n\n"

text = "Das ist ein Text.";

if re.search(r"(?i)IsT", text): # sucht "IsT" unabhängig von Klein- und Großschreibung (?i)
  print "Gefunden!"
else:
  print "Nicht gefunden!"
```

### Beispiel #4

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import re

print "Content-type: text/plain\n\n"

text = 'Das " ist das Trennzeichen für Anfang und Ende.';

if re.search(r"\"", text): # sucht "; das " muss maskiert werden
  print "Gefunden!"
else:
  print "Nicht gefunden!"
```

### Beispiel #5

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import re

print "Content-type: text/plain\n\n"

text = "Das ist ein Text.";

if re.search(r"ist|ein", text): # sucht "ist" oder (|) "ein"
  print "Gefunden!"
else:
  print "Nicht gefunden!"
```

### Siehe auch

- [Reguläre Ausdrücke in Perl](/perl/regulaere-ausdruecke-perl){:target="_blank"}
- [Reguläre Ausdrücke in Ruby](/ruby/regulaere-ausdruecke-ruby){:target="_blank"}
