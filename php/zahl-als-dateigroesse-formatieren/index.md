---
title: Zahl als Dateigröße formatieren (PHP)
---

## Zahl als Dateigröße formatieren (PHP)

### Funktion

```php
<?php
  function format_filesize($size) {
    $arr_units = array(
      '<acronym lang="en" xml:lang="en" title="Byte">B</acronym>',
      '<acronym lang="en" xml:lang="en" title="Kilobyte">KB</acronym>',
      '<acronym lang="en" xml:lang="en" title="Megabyte">MB</acronym>',
      '<acronym lang="en" xml:lang="en" title="Gigabyte">GB</acronym>',
      '<acronym lang="en" xml:lang="en" title="Terabyte">TB</acronym>'
    );
    for ($i = 0; $size > 1024; $i++) {
      $size /= 1024;
    }
    return number_format($size, 2, ',', '').' '.$arr_units[$i];
  }
?>
```

### Beispiel

```php
<?php
  // Dateigröße ermitteln
  $i_size = filesize($_SERVER['DOCUMENT_ROOT'].'/file.pdf');
  // Dateigröße formatieren und ausgeben
  echo format_filesize($i_size);
?>
```
