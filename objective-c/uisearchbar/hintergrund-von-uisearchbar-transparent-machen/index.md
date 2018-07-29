---
title: Hintergrund von UISearchBar transparent machen
---

## Hintergrund von UISearchBar transparent machen

Das folgende Beispiel zeigt, wie man den Hintergrund einer `UISearchBar` transparent machen kann.

```objective_c
self.searchBar.translucent = YES;
self.searchBar.backgroundImage = [UIImage new];
self.searchBar.scopeBarBackgroundImage = [UIImage new];
```
