---
title: Sehr sichere Kennwort-Hashs mit PHP erstellen
---

## Sehr sichere Kennwort-Hashs mit PHP erstellen

### PHP-Funktion

```php
<?php
  function generate_password_hash($str_password, $str_username) {
    $arr_password = (array) str_split( $str_password, (strlen($str_password)/2)+1 );
    $str_middle_salt = (string) 'd033e22ae348aeb5660fc21422ae348aeb5660fc2140aec35850c4da997';
    $str_hash = (string) hash( 'whirlpool', $str_username.$arr_password[0].$str_middle_salt.$arr_password[1] );
    return $str_hash;
  }
?>
```

### Anwendungsbeispiel

```php
<?php
  $str_hash = (string) generate_password_hash('bar', 'foo');
  echo $str_hash;

  /*
    Ausgabe:
    2fdd22fef44c97a863d0b19d6a6233a53891a0d31448b91a15751ad2adb85644c721ea89d8438c5090c051996cbbd3a34d24887165661d7ba60aa661597f12e2
  */
?>
```

### Weiterführende Informationen

- [PHP-Funktion hash()](http://de.php.net/manual/de/function.hash.php){:target="_blank"}
- [Wikipedia: Whirlpool (Algorithmus)](http://de.wikipedia.org/wiki/Whirlpool_%28Algorithmus%29){:target="_blank"}
- [Offizielle WHIRLPOOL Homepage](http://www.larc.usp.br/%7Epbarreto/WhirlpoolPage.html){:target="_blank"}
