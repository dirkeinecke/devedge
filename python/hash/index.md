---
title: Hash
---

## Hash

### Beispiel #1 - MD5 (Message-Digest Algorithm 5) Hash

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import hashlib

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

h = hashlib.md5(text)
print h.hexdigest() # Ausgabe: 232d23d543143fc45c14f0c544a93257
```

### Beispiel #2 - SHA-1 (Secure Hash Algorithm 1) Hash

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import hashlib

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

h = hashlib.sha1(text)
print h.hexdigest() # Ausgabe: 06f3f3a05fcb165aab5232b1753fd54f4e6ace06
```

### Beispiel #3 - SHA-224 (Secure Hash Algorithm 224) Hash

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import hashlib

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

h = hashlib.sha224(text)
print h.hexdigest() # Ausgabe: 19b389ef8b890ab10caa8acd0e2628124b8cb8dfcd142a1263d20c86
```

### Beispiel #4 - SHA-254 (Secure Hash Algorithm 254) Hash

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import hashlib

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

h = hashlib.sha256(text)
print h.hexdigest() # Ausgabe: e7740bb3ed5d4697f423cc0016bc58ec897f36b481307986fd8c42919d15a85b
```

### Beispiel #5 - SHA-384 (Secure Hash Algorithm 384) Hash

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import hashlib

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

h = hashlib.sha384(text)
print h.hexdigest() # Ausgabe: 700fe60be964fcb7938f9a03da4f8ce640dd9b3fc07f163c17ef103d991db92bc47608a8fcd5e7aead1bd72982c5689a
```

### Beispiel #5 - SHA-512 (Secure Hash Algorithm 512) Hash

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import hashlib

print "Content-type: text/plain\n\n"

text = "Das ist ein Text."

h = hashlib.sha512(text)
print h.hexdigest() # Ausgabe: 09d70b4207a711ea8f978b89ca76904b0b9bc6f34c69ee0ef61e8ca8c0e46977fb0e9343aa5dbd540838fcd7b380511987fda579d5511c1370d9218291b75ecc
```

### Weiterführende Informationen

- [Message-Digest Algorithm 5](https://de.wikipedia.org/wiki/Message-Digest_Algorithm_5){:target="_blank"}
- [Wikipedia: Secure Hash Algorithm](https://de.wikipedia.org/wiki/Secure_Hash_Algorithm){:target="_blank"}
