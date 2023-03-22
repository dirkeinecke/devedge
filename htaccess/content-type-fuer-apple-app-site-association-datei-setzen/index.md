---
title: Content-Type für apple-app-site-association Datei setzen
---

## Content-Type für "apple-app-site-association"-Datei setzen

Wenn man den Content-Type für eine "apple-app-site-association"-Datei setzen möchte, dann kann man dies mitels einer der folgenden beiden Varianten tun:

### Variante 1

```
<FilesMatch "^apple-app-site-association$">
  ForceType application/json
</FilesMatch>
```
### Variante 2

```
RewriteEngine On
RewriteRule ^apple-app-site-association$ - [env=apple:1]
Header set Content-type application/json env=apple
```

### Weiterführende Informationen

- [Apache-Kernfunktionen: ForceType-Direktive](https://httpd.apache.org/docs/trunk/mod/core.html#forcetype){:target="_blank"}
- [Apache Module mod_headers](https://httpd.apache.org/docs/trunk/mod/mod_headers.html){:target="_blank"}