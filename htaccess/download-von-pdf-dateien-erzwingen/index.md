## Download von PDF-Dateien erzwingen

Wenn man den Download von PDF-Dateien erzwingen möchte,
dann mus man folgende Zeile der .htaccess-Datei hinzufügen:

```apache_conf
AddType application/octet-stream .pdf
<FilesMatch "\.(PDF|pdf)$" >
  ForceType application/octet-stream
  Header set Content-Disposition: attachment
</FilesMatch>
```

### Weiterführende Informationen

- [Apache Module mod_mime: AddType Directive](https://httpd.apache.org/docs/trunk/mod/mod_mime.html#addtype){:target="_blank"}
- [Apache-Kernfunktionen: ForceType-Direktive](https://httpd.apache.org/docs/trunk/mod/core.html#forcetype){:target="_blank"}
