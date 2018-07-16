## Umleitung anhand der Sprache des Browsers

```
RewriteCond %{HTTP:Accept-Language} (de) [NC]
RewriteRule ^/?$ /de/ [R,NC,L]
RewriteRule ^/?$ /en/ [R,NC,L]
```
