---
title: Bedingungen
---

## Bedingungen

### Beispiel #1 - Inhalt nur auf Startseite anzeigen

```xml
<b:if cond='data:blog.pageType == &quot;index&quot;'>
  Dieser Text wird nur auf der Startseite angezeigt.
</b:if>
```

### Beispiel #2 - Inhalt nicht auf Startseite anzeigen

```xml
<b:if cond='data:blog.pageType != &quot;index&quot;'>
  Dieser Text wird nur auf der Startseite angezeigt.
</b:if>
```

### Beispiel #3 - Inhalt nur auf Einzelpost-Seiten anzeigen

```xml
<b:if cond='data:blog.pageType == &quot;item&quot;'>
  Dieser Text wird nur auf der Einzelpost-Seiten angezeigt.
</b:if>
```

### Beispiel #4 - Inhalt nicht auf Einzelpost-Seiten anzeigen

```xml
<b:if cond='data:blog.pageType != &quot;item&quot;'>
  Dieser Text wird nur auf der Einzelpost-Seiten angezeigt.
</b:if>
```

### Beispiel #5 - Inhalt nur auf Archiv-Seiten anzeigen

```xml
<b:if cond='data:blog.pageType == &quot;archive&quot;'>
    Dieser Text wird nur auf Archiv-Seiten angezeigt.
</b:if>
```

### Beispiel #6 - Inhalt nicht auf Archiv-Seiten anzeigen

```xml
<b:if cond='data:blog.pageType == &quot;archive&quot;'>
    Dieser Text wird nur auf Archiv-Seiten angezeigt.
</b:if>
```

### Beispiel #7 - Inhalt nur anzeigen, wenn bestimmtes Label gesetzt wurde

```xml
<b:if cond='data:post.labels'>
  <b:loop values='data:post.labels' var='label'>
    <b:if cond='data:label.name == &quot;Video&quot;'>
      Dieser Text wird nur angezeigt, wenn das Label 'Video' gesetzt wurde.
    </b:if>
  </b:loop>
</b:if>
```
