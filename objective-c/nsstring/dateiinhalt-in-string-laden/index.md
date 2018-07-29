---
title: Dateiinhalt in String laden
---

## Dateiinhalt in String laden

Das folgende Beispiel zeigt, wie man den Inhalt einer Datei in einen String laden kann.

```objective_c
NSError *error = nil;
NSString *html = [[NSString alloc] initWithContentsOfFile:[[NSBundle mainBundle] pathForResource:@"MyFile" ofType:@"html"] encoding:NSUTF8StringEncoding error:&error];
```

## Weiterführende Informationen
- [Mac OS X Reference Library: NSString Class Reference](https://developer.apple.com/documentation/foundation/nsstring){:target="_blank"}
