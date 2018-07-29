---
title: UITableView lässt sich nicht scrollen
---

## UITableView lässt sich nicht scrollen

Wenn man einer `UITableView` einen Search Display Controller hinzufügt und nur wenige Einträge in der `UITableView` vorhanden sind, dann kann man u. U. die TableView nicht mehr scrollen. Dieses Problem kann man beseitigen, in dem man folgenden Code in die Methode `viewDidLoad()` einfügt:

```objective_c
[self.tableView setBounces:YES];
```

## Weiterführende Informationen

- [UITableView Class Reference](https://developer.apple.com/documentation/uikit/uitableview){:target="_blank"}
- [UISearchDisplayController Class Reference](https://developer.apple.com/documentation/uikit/uisearchdisplaycontroller){:target="_blank"}
