---
title: Seiten mit einem bestimmten Parameter umleiten
---

## Seiten mit einem bestimmten Parameter umleiten

```
Options +FollowSymlinks
RewriteEngine On

RewriteCond %{QUERY_STRING} .*we_objectID=69.* [NC]
RewriteRule (.*) http://www.domain.de/foo/bar.html? [R=301,L]
```
