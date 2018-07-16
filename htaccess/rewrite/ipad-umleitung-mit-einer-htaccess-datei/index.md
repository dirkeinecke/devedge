## iPad Umleitung mit einer .htaccess-Datei

```apache_conf
Options +FollowSymlinks
RewriteEngine On

RewriteCond %{HTTP_USER_AGENT} ^.*iPad.*$
RewriteRule ^(.*)$ http://ipad.domain.de [R=301]
```
