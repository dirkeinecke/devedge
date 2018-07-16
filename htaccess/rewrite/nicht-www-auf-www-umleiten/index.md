## nicht-www auf www umleiten

Das folgende Beispiel zeigt, wie man alle Aufrufe ohne "`www`" (`http://domain.de`) auf die
Domain mit "`www`" (`http:/www.domain.de`) umleiten kann. Dabei müssen Aufrufe über "`http`"
und "`https`" gesondert behandelt werden.

```apache_conf
RewriteEngine on

RewriteCond %{HTTPS} off
RewriteCond %{HTTP_HOST} !^www\.(.*)$ [NC]
RewriteRule ^(.*)$ http://www.%{HTTP_HOST}/$1 [R=301,L]

RewriteCond %{HTTPS} on
RewriteCond %{HTTP_HOST} !^www\.(.*)$ [NC]
RewriteRule ^(.*)$ https://www.%{HTTP_HOST}/$1 [R=301,L]
```
