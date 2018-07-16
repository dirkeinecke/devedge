## Umleitung anhand der Sprache des Browsers

```apache_conf
RewriteCond %{HTTP:Accept-Language} (de) [NC]
RewriteRule ^/?$ /de/ [R,NC,L]
RewriteRule ^/?$ /en/ [R,NC,L]
```
