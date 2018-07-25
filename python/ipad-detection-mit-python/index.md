---
title: iPad Detection mit Python
---

## iPad Detection mit Python

```python
#!/usr/bin/env python
import cgi
import os

print "Content-Type: text/html\n"

ua = os.environ['HTTP_USER_AGENT']

def detect_ipad():
  if ua.find('iPad') != -1:
    return True
  else:
    return False

if detect_ipad() == True:
  print '<p style="font-size: 30px">This is an iPad.</p>'
else:
  print '<p style="font-size: 30px">This is not an iPad.</p>'
```
