---
title: Weiches Scrollen zu einem bestimmten Element
---

## Weiches Scrollen zu einem bestimmten Element

Das folgende Beispiel zeigt, wie man programmiertechnisch mittels der Effekte von jQuery
in einer festgelegten Geschwindigkeit weich zu einem bestimmten Element scrollen lassen kann.

```javascript
$('html, body').animate({
  scrollTop: $('#ELEMENT_ID').offset().top
}, 200);
```

### Weiterführende Informationen

- [jQuery API-Website - Effekte - .animate()](https://api.jquery.com/animate/){:target="_blank"}
