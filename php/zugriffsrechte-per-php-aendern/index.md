---
title: Zugriffsrechte per PHP ändern
---

## Zugriffsrechte per PHP ändern

Mit PHP werden Zugriffsrechte für Dateien und Verzeichnisse mit der Funktion chmod() geändert.

### Beispiel #1 – Zugriffsrechte für eine Datei ändern

```php
<?php
  chmod($_SERVER['DOCUMENT_ROOT'] . '/datei.php', 0777);
?>
```

### Beispiel #2 – Zugriffsrechte für alle Dateien in einem Verzeichnis rekursiv ändern

```php
<?php
  function recursive_chmod($foldername, $dir_mode, $file_mode) {
     $dh = opendir($foldername);
 
     while($entry = readdir($dh)) {
       if ('' != $entry && '.' != $entry && '..' != $entry) {
         $_entry = $foldername . '/' . $entry;
 
         if (!is_dir($_entry)) {
           chmod($_entry, $file_mode);
         }
 
         if (is_dir($_entry)) {
           recursive_chmod($_entry, $dir_mode, $file_mode);
         }
       }
     }
     closedir($dh);
     chmod($foldername, $dir_mode);
  }
 
  recursive_chmod($_SERVER['DOCUMENT_ROOT'] . '/verzeichnisname', 0755, 0644);
?>
```

### Weiterführende Informationen

- [PHP-Referenz: chmod()](http://de3.php.net/manual/de/function.chmod.php){:target="_blank"}
- [php-faq.de: Unix - Welche Zugriffsrechte brauche ich, um eine Datei anzulegen?](http://www.php-faq.de/q/q-datei-rechte.html){:target="_blank"}
