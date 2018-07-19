---
title: Microsoft Internet Explorer gibt Wert des "src"-Attributs bei Abfrage des "href"-Attributs bei Bildern aus
---

## Microsoft Internet Explorer gibt Wert des "src"-Attributs bei Abfrage des "href"-Attributs bei Bildern aus

### Testumgebung

- Microsoft Windows XP Home Edition Version 2002 Service Pack 3
- Microsoft Internet Explorer 6

### Quellcode

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
        "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="de" lang="de">
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
    <title></title>
    <meta name="description" content="" />
    <meta name="keywords" content="" />
  </head>
  <body>
    <img src="foobar.jpg" id="myImage" />
    <script type="text/javascript">alert(document.getElementById('myImage').href);</script>
  </body>
</html>
```

### Ausgabe in der Alert-Box

```
http://www.domain.de/foobar.jpg
```
