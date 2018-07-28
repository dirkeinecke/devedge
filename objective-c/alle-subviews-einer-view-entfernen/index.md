---
title: Alle Subviews einer View entfernen
---

## Alle Subviews einer View entfernen

Das folgende Beispiel zeigt, wie man alle Subviews einer View entfernen kann.

```objective_c
for (UIView *view in [[self myView] subviews]) {
  [view removeFromSuperview];
}
```
