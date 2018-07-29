---
title: Mehrere Bar Button Items setzen
---

## Mehrere Bar Button Items setzen

Seit iOS 5 kann man mehrere Bar Button Items mit einem Methodenaufruf setzen. Entwickelt man eine App aber auch für iOS < 5, muss man dabei eine Unterscheidung für ältere iOS-Versionen einbauen.

```objective_c
if ([[self navigationItem] respondsToSelector:@selector(setRightBarButtonItems:)]) {
  UIBarButtonItem *button1 = [[UIBarButtonItem alloc] initWithBarButtonSystemItem:UIBarButtonSystemItemSearch target:self action:@selector(foo)];
  UIBarButtonItem *button2 = [[UIBarButtonItem alloc] initWithBarButtonSystemItem:UIBarButtonSystemItemAction target:self action:@selector(bar)];
  [[self navigationItem] setRightBarButtonItems:[NSArray arrayWithObjects:foo, bar, nil] animated:YES];
} else {
  UIBarButtonItem *button = [[UIBarButtonItem alloc] initWithBarButtonSystemItem:UIBarButtonSystemItemAction target:self action:@selector(bar)];
  [[self navigationItem] setRightBarButtonItem:button animated:YES];
}
```

## Weiterführende Informationen

- [NSObject Protocol Reference](https://developer.apple.com/documentation/objectivec/1418956-nsobject){:target="_blank"}
- [UINavigationItem Class Reference](https://developer.apple.com/documentation/uikit/uinavigationitem){:target="_blank"}
