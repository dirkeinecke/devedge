---
title: Packen
---

## Packen

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import gzip

print "Content-type: text/plain\n\n"

f = gzip.open("test.gz", "wb")
f.write("Das ist ein Text.")
f.close()
```
