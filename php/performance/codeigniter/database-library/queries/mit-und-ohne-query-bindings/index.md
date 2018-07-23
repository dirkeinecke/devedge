---
title: Mit und ohne Query Bindings
---

## Mit und ohne Query Bindings

### Quelltext ohne Query Bindings

```php
<?php
  class qbtest extends Controller {
    function __construct() {
      parent::Controller();
    }
        
    function index() {
      $start = microtime(true);

      for ( $i = 1; $i <= 10000; $i++ ) {
        $this->db->query('SELECT * FROM users WHERE id = 1');
      }

      $end = microtime(true);

      echo '<br>';
      echo $end - $start;
    }
  }
?>

### Ergebnis ohne Query Bindings

```
0.90828704833984
```

### Quelltext mit Query Bindings

```php
<?php
  class qbtest extends Controller {
    function __construct() {
      parent::Controller();
    }
        
    function index() {
      $start = microtime(true);

      for ( $i = 1; $i <= 10000; $i++ ) {
        $this->db->query('SELECT * FROM users WHERE id = ?', array(1));
      }

      $end = microtime(true);

      echo '<br>';
      echo $end - $start;
    }
  }
?>
```

### Ergebnis mit Query Bindings

```
1.0285220146179
```

### Weiterführende Informationen

- [CodeIgniter User Guide Home - Database Library - Queries](http://codeigniter.com/user_guide/database/queries.html){:target="_blank"}
