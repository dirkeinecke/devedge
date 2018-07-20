---
title: foreach-Schleife
---

## foreach-Schleife

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

@text = ('Hallo', 'Welt');

foreach $text (@text) {
  print $text;
  print ' ';
}
```
