---
title: .htaccess
---

## .htaccess

{% assign originPagePath = page.path %}
{% assign originPagePathParts = page.path | split: "/" %}
{% assign originSize = originPagePathParts.size %}
{% assign pagePath = page.path | remove: "index.md" %}
{{ pagePath }}

8

{% for page in site.pages %}
  {% if page.path != originPagePath %}
    {% if page.path contains pagePath %}
      {% assign pagePathParts = page.path | split: "/" %}
      {% assign size = pagePathParts.size %}
      {% if size <= originSize %}
        {{ page.path }}
      {% endif %}
    {% endif %}
  {% endif %}
{% endfor %}

- [Alle Verzeichnisse und Dateien von einer Domain auf eine andere Domain umleiten](alle-verzeichnisse-und-dateien-von-einer-domain-auf-eine-andere-domain-umleiten)
- [Benutzerdefinierte Fehlerseiten](benutzerdefinierte-fehlerseiten)
- [Download von PDF-Dateien erzwingen](download-von-pdf-dateien-erzwingen)
- [MIME-Type für manifest-Dateien setzen](mime-type-fuer-manifest-dateien-setzen)
- [Rewrite](rewrite)
