---
title: Zendesk-Dopbox bei Seitenaufruf öffnen
---

## Zendesk-Dopbox bei Seitenaufruf öffnen

Möchte man auf der eigenen Seite die Dropbox von Zendesk gleich beim Seitenaufruf öffnen, dann kann man dies wie folgt realisieren:

### URL

```
http://www.doamin.tld/datei.html#support
```

### Quelltext (direkt nach dem Quelltext der Integration für die Zendesk-Dropbox einfügen)

```javascript
<script type="text/javascript">
  if (window.location.hash == '#support') {
    Zenbox.render();
  }
</script>
```
