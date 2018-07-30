---
title: Fehler von Form Validation als Liste ausgeben
---

## Fehler von Form Validation als Liste ausgeben

Möchte man die Fehler einer Formularüberprüfung (Library “Form Validation”) als HTML-Liste (`<ul>...</ul>`) ausgeben, kann man dies nicht über die von der Library zur Verfügung gestellten Funktion `validation_errors()` realisieren. Um dies zu erreichen muss man zunächst die Tennzeichen leeren, alle Fehler über die Funktion `form_error()` in ein eigenes PHP-Array schreiben, dieses von leeren Einträgen bereinigen und kann dieses dann im View ausgeben.

### Controller

```php
// Trennzeichen leeren
$this->form_validation->set_error_delimiters('', '');

// Fehlermeldungen in ein temporäres PHP-Array schreiben
$arr_errors = (array) array(
  (string) form_error('name'),
  (string) form_error('email'),
  (string) form_error('url'),
  (string) form_error('text')
);

// Leeren Einträge aus dem temporären PHP-Array entfernen
$arr_data['arr_errors'] = (array) array();
foreach ( $arr_errors as $str_error ) {
  if ( '' != $str_error ) {
    $arr_data['arr_errors'][] = (string) $str_error;
  }
}

// View aufrufen und Daten an dieses übergeben
$this->load->view('my_view', $arr_data);
```

### View

```php
// Ausgabe der Fehler als HTML-Liste
if ( isset($arr_errors) && is_array($arr_errors) && 0 < count($arr_errors) ) {
  echo '<ul>';
  foreach ( $arr_errors as $str_error ) {
    echo '<li>', $str_error, '</li>';
  }
  echo '</ul>';
}
```

## Weiterführende Informationen

- [CodeIgniter User Guide - Form Validation](https://codeigniter.com/user_guide/libraries/form_validation.html){:target="_blank"}
