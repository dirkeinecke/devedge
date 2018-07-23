---
title: Variable versus Konstante
---

## Variable versus Konstante

### Testumgebung

iMac, 2.8 GHz Intel Core i7, 4 GB RAM, Apache 2.0.63, PHP 5.2.11

### Quelltext für Variable

```php
<?php
  $start = microtime(true);

  $variable = 'Hallo Welt!';

  for ( $i = 1; $i <= 1000000; $i++ ) {
    echo $variable;
  }

  $end = microtime(true);

  echo '<br>';
  echo $end - $start;
?>
```

### Ergebnis für Variable

```
0.187422990799
```

### Quelltext für Konstante

```php
<?php
  $start = microtime(true);

  define('KONSTANTE', 'Hallo Welt!');

  for ( $i = 1; $i <= 1000000; $i++ ) {
    echo KONSTANTE;
  }

  $end = microtime(true);

  echo '<br>';
  echo $end - $start;
?>
```

### Ergebnis für Konstante

```
0.283890008926
```

### Weiterführende Informationen

- [PHP-Referenz: echo](http://de.php.net/manual/de/function.echo.php){:target="_blank"}
- [PHP-Referenz: define()](http://de2.php.net/manual/de/function.define.php){:target="_blank"}
- [PHP-Referenz: microtime()](http://de.php.net/manual/de/function.microtime.php){:target="_blank"}
