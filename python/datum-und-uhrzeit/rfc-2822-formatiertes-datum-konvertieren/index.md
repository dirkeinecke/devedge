---
title: RFC 2822 formatiertes Datum konvertieren
---

## RFC 2822 formatiertes Datum konvertieren

### Beispiel #1 - in Tupel konvertieren

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from email.utils import parsedate_tz

print "Content-type: text/plain\n\n"

d1 = "Sat, 31 Jan 2009 20:47:20 +0100" # RFC 2822
d2 = parsedate_tz(d1) # Tuple

print d2 # Ausgabe: (2009, 1, 31, 20, 47, 20, 0, 1, -1, 3600)
```

### Beispiel #2 - in Unix Timestamp konvertieren

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from email.utils import parsedate_tz, mktime_tz

print "Content-type: text/plain\n\n"

d1 = "Sat, 31 Jan 2009 20:47:20 +0100" # RFC 2822
d2 = parsedate_tz(d1) # Tuple
d3 = mktime_tz(d2) # Unix Timestamp

print d3 # Ausgabe: 1233431240.0
print int(d3) # Ausgabe: 1233431240
```

### Beispiel #3

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from email.utils import parsedate
from time import strftime

print "Content-type: text/plain\n\n"

d1 = "Sat, 31 Jan 2009 20:47:20 +0100" # RFC 2822
d2 = parsedate(d1) # Tuple
d3 = strftime("%d.%m.%Y %H:%M:%S", d2) + ' Uhr'

print d3 # Ausgabe: 31.01.2009 20:47:20 Uhr
```

### Weiterführende Informationen

- [RFC 2822](http://www.faqs.org/rfcs/rfc2822){:target="_blank"}
- [The Python Standard Library - time — Time access and conversions](https://docs.python.org/library/time.html){:target="_blank"}
- [The Python Standard Library - email: Miscellaneous utilities](https://docs.python.org/library/email.util.html){:target="_blank"}
