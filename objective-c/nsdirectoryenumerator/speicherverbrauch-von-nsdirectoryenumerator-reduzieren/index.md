---
title: Speicherverbrauch von NSDirectoryEnumerator reduzieren
---

## Speicherverbrauch von NSDirectoryEnumerator reduzieren

Bei der Verwendung eines NSDirectoryEnumerator ist zu beachten, dass man innerhalb der while-Schleife einen separaten autorelease-Pool (NSAutoreleasePool) verwendet, da ein autoreleased String zurückgegeben wird.

### NSDirectoryEnumerator mit steigendem Speicherverbrauch

```objective_c
NSDirectoryEnumerator* direnum = [fileManager enumeratorAtPath:path];
 
NSString* entry;
while (entry = [direnum nextObject]) {
  // ...
}
```

### NSDirectoryEnumerator mit konstantem Speicherverbrauch

```objective_c
NSDirectoryEnumerator* direnum = [fileManager enumeratorAtPath:path];
NSAutoreleasePool *innerPool = [[NSAutoreleasePool alloc] init];
 
NSString* entry;
while (entry = [direnum nextObject]) {
  // ...
  [innerPool release];
  innerPool = [[NSAutoreleasePool alloc] init];
}
innerPool = nil;
```

### Weiterführende Informationen

- [Mac OS X Reference Library: NSDirectoryEnumerator Class Reference](https://developer.apple.com/documentation/foundation/filemanager/directoryenumerator){:target="_blank"}
- [Mac OS X Reference Library: NSAutoreleasePool Class Reference](https://developer.apple.com/documentation/foundation/nsautoreleasepool){:target="_blank"}
