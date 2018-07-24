---
title: Bibliotheken einbinden
---

## Bibliotheken einbinden

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import math

print "Content-type: text/plain\n\n"

print math.sin(math.pi) # Ausgabe: 1.22460635382e-16
```

### Beispiel #2 - Namen des Namensraums festlegen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import math as mathematik

print "Content-type: text/plain\n\n"

print mathematik.sin(mathematik.pi) # Ausgabe: 1.22460635382e-16
```

### Beispiel #3 - ohne Namensraum

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from math import *

print "Content-type: text/plain\n\n"

print sin(pi) # Ausgabe: 1.22460635382e-16
```

### Beispiel #4 - ohne Namensraum mit Angabe der zu importierenden Elemente

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from math import sin, pi

print "Content-type: text/plain\n\n"

print sin(pi) # Ausgabe: 1.22460635382e-16
```
