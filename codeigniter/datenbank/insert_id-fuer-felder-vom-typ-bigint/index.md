---
title: insert_id() für Felder vom Typ BIGINT
---

## insert_id() für Felder vom Typ BIGINT

Die Methode `insert_id()` (in /system/database/drivers/mysql/mysql_driver.php) funktioniert für Felder vom Typ `BIGINT` nicht, da sie die PHP-Funktion `mysql_insert_id()` verwendet.

Falls Ihre `AUTO_INCREMENT` Spalte vom Typ `BIGINT` (64 Bit) ist, ist der Wert den `mysql_insert_id()` liefert, nicht korrekt. Verwenden Sie in diesem Fall stattdessen die MySQL interne SQL Funktion `LAST_INSERT_ID()` in einer SQL-Abfrage.

Dieses Problem kann man umgehen, in dem man die Methode `insert_id()` anpasst.

### Original:

```php
/**
 * Insert ID
 *
 * @access public
 * @return integer
 */
function insert_id()
{
    return @mysql_insert_id($this->conn_id);
}
```

### Angepasste Version:

```php
/**
 * Insert ID
 *
 * @access public
 * @return integer
 */
function insert_id()
{
    //return @mysql_insert_id($this->conn_id);
    $query = $this->query('SELECT LAST_INSERT_ID() AS id');
    if ($query->num_rows() > 0) {
        foreach ($query->result_array() as $row) {
            return $row['id'];
        }
    } else {
        return 0;
    }
}
```

## Weiterführende Informationen

- [PHP-Referenz: `mysql_insert_id()`](http://www.php.net/mysql_insert_id){:target="_blank"}
