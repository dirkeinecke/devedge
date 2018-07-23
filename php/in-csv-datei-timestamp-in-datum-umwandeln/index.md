---
title: In CSV-Datei Timestamp in Datum umwandeln
---

## In CSV-Datei Timestamp in Datum umwandeln

Hinweis: Feld mit Timestamp muss das erste Feld sein.

```php
<?php
  $str_filename = (string) 'datei.csv';
  $str_content = (string) file_get_contents($str_filename);
  $arr_content = (array) explode("\n", $str_content);

  $str_file = (string) ''; // Wenn erste Zeile Feldnamen enthält, dann hier diese einsetzen

  for ($i = 0; $i <= count($arr_content); $i++) { // Wenn erste Zeile Feldnamen enthält, dann ab 1
    $i_date = substr($arr_content[$i], 0, 10);
    $str_file .= str_replace($i_date, date('d.m.Y', $i_date), $arr_content[$i]) . "\n";
  }

  file_put_contents('_'.$str_filename, $str_file);
?>
```
