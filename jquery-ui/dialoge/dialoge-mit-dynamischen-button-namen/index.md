## Dialoge mit dynamischen Button-Namen

{% assign pagePathParts = page.path | split: "/" %}
{% assign size = pagePathParts.size | minus: 3 %}

<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item" href="{{ "/" | relative_url }}">Home</li>
{% assign comparePathWithoutFilename = "" %}
{% for i in (0..size) %}
  {% assign comparePathWithoutFilename = comparePathWithoutFilename | append: pagePathParts[i] | append: "/" %}
  {% assign p = comparePathWithoutFilename | append: "index.md" %}
  {% for page in site.pages %}
    {% if page.path == p %}
      <li class="breadcrumb-item"><a href="{{ page.path }}">{{ page.title }}</a></li>
    {% endif %}
  {% endfor %}
{% endfor %}
  </ol>
</nav>


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
