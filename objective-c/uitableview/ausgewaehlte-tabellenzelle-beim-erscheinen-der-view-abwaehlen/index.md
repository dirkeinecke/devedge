---
title: Ausgewählte Tabellenzelle beim Erscheinen der View abwählen
---

## Ausgewählte Tabellenzelle beim Erscheinen der View abwählen

Um die ausgewählte Tabellenzelle beim Erscheinen der View abzuwählen, geht man wie folgt vor:

```objective_c
- (void)viewWillAppear:(BOOL)animated {
  [super viewWillAppear:animated];

  NSIndexPath *indexPath = [tableView indexPathForSelectedRow];
  if (indexPath) {
    [tableView deselectRowAtIndexPath:indexPath animated:YES];
  }
}
```

## Weiterführende Informationen

- [UITableView Class Reference](https://developer.apple.com/documentation/uikit/uitableview){:target="_blank"}
