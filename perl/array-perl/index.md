---
title: Array
---

## Array

### Beispiel #1

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

@text = ("Hallo", "Welt");

print $text[0];
print " ";
print $text[1];
```

### Beispiel #2

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

@text = ();
$text[0] = "Hallo";
$text[1] = "Welt";

print $text[0];
print " ";
print $text[1];
```
