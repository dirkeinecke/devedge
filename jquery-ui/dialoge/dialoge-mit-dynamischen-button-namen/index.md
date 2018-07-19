## Dialoge mit dynamischen Button-Namen

{{ page.path }}

{% assign pagePathParts = page.path | split: "/" %}
{% assign size = pagePathParts.size | minus: 3 %}

{{ size }}

{% for i in (0..size) %}
  {% for page in site.pages %}
    {% assign p = pagePathParts[i] | append: "/index.md" %}
    {{ p }}
    {% if page.path == p %}
      {{ page.path }}
    {% endif %}
  {% endfor %}
{% endfor %}

3

```javascript
var error_dialog_buttons = {};
error_dialog_buttons[lang.ok] = function() {
  $(this).dialog('close');
};

$('#error_dialog').dialog({
  autoOpen: false,
  modal: true,
  show: null,
  hide: null,
  resizable: false,
  draggable: false,
});

$('#error_dialog').dialog({buttons:error_dialog_buttons});
```

### Weiterführende Informationen

- [jQuery UI Website](https://jqueryui.com/){:target="_blank"}
- [jQuery UI Website - Dialog](https://jqueryui.com/dialog/){:target="_blank"}
