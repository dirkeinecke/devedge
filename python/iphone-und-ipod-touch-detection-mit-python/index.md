---
title: iPhone und iPod touch Detection mit Python
---

## iPhone und iPod touch Detection mit Python

```python
#!/usr/bin/env python
import cgi
import os

print "Content-Type: text/html\n"

ua = os.environ['HTTP_USER_AGENT']

def detect_iphone():
  if ua.find('iPhone') != -1 or ua.find('iPod') != -1:
    return True
  else:
    return False

if detect_iphone() == True:
  print '<p style="font-size: 30px">This is an iPhone or iPod touch.</p>'
else:
  print '<p style="font-size: 30px">This is not an iPhone or iPod touch.</p>'
```
