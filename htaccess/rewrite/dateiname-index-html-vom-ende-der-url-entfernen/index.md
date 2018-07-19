---
title: Dateiname index.html vom Ende der URL entfernen
---

## Dateiname index.html vom Ende der URL entfernen

```
# Remove index.html from the end of the url
RewriteRule ^index\.html$ / [R=301,L]
RewriteRule ^(.*)/index\.html$ /$1/ [R=301,L]
```
