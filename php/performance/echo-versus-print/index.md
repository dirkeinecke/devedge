---
title: echo versus print
---

## echo versus print

### Testumgebung

iMac, 2.8 GHz Intel Core i7, 4 GB RAM, Apache 2.0.63, PHP 5.2.11

### Quelltext für echo

```php
<?php
  $start = microtime(true);

  for ( $i = 1; $i <= 10000000; $i++ ) {
    echo 1;
  }

  $end = microtime(true);

  echo '<br>';
  echo $end - $start;
?>
```

### Ergebnis für echo

```
2.17717790604
```

### Quelltext für print

```php
<?php
  $start = microtime(true);

  for ( $i = 1; $i <= 10000000; $i++ ) {
    print 1;
  }

  $end = microtime(true);

  echo '<br>';
  echo $end - $start;
?>
```

### Ergebnis für print

```
2.27813196182
```

### Weiterführende Informationen

- [PHP-Referenz: echo](http://de.php.net/manual/de/function.echo.php){:target="_blank"}
- [PHP-Referenz: print](http://de.php.net/manual/de/function.print.php){:target="_blank"}
- [PHP-Referenz: microtime(http://de.php.net/manual/de/function.microtime.php)](){:target="_blank"}
