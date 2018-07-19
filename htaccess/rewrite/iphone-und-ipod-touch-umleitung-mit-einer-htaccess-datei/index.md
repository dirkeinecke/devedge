---
title: iPhone Umleitung mit einer .htaccess-Datei
---

## iPhone Umleitung mit einer .htaccess-Datei

```
Options +FollowSymlinks
RewriteEngine On

RewriteCond %{HTTP_USER_AGENT} ^.*iPhone.*$
RewriteRule ^(.*)$ http://iphone.domain.de [R=301]
```
