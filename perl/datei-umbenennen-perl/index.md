---
title: Datei umbenennen
---

## Datei umbenennen

```perl
#!/usr/local/bin/perl

use CGI::Carp 'fatalsToBrowser';

print "Content-type: text/html\n\n";

$alt = 'foo.html';
$neu = 'bar.html';

rename $alt, $neu or die "Konnte die Datei $alt nicht in $neu umbenennen: $!";
```
