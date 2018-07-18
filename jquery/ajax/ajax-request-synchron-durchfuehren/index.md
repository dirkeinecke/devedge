## Ajax-Request synchron durchführen

Möchte man einen Ajax-Request mit jQuery synchron durchführen, kann man dies über `$.ajaxSetup` wie folgt festlegen:

```javascript
$.ajaxSetup({
  async:false
});
```

### Weiterführende Informationen

- [jQuery-Dokumentation: jQuery.ajax()](https://api.jquery.com/jQuery.ajax/){:target="_blank"}
- [jQuery-Dokumentation: jQuery.ajaxSetup()](https://api.jquery.com/jQuery.ajaxSetup/){:target="_blank"}
