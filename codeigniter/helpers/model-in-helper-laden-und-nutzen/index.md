---
title: Model in Helper laden und nutzen
---

## Model in Helper laden und nutzen

Das folgende Beispiel zeigt, wie man ein Model innerhalb eines Helpers laden und nutzen kann.

```php
function my_helper_function() {
  $CI =& get_instance();
  $CI->load->model('mymodel');
  $var = $CI->mymodel->whatever();
}
```

## Weiterführende Informationen

- [CodeIgniter User Guide - Helper Functions](https://codeigniter.com/user_guide/general/helpers.html){:target="_blank"}
