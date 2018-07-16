## iPod touch Umleitung mit einer .htaccess-Datei

```apache_conf
Options +FollowSymlinks
RewriteEngine On

RewriteCond %{HTTP_USER_AGENT} ^.*iPod.*$
RewriteRule ^(.*)$ http://ipod.domain.de [R=301]
```
