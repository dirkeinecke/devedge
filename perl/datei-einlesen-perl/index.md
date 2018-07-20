---
title: Datei einlesen
---

## Datei einlesen

```perl
#!/usr/local/bin/perl

use CGI::Carp 'fatalsToBrowser'; # Fehler sollen im Browser ausgegeben werden

print "Content-type: text/html\n\n";

$datei = 'testdatei.txt';

open IN, $datei or die "Kann $datei nicht zum Lesen oeffnen: $!";
while ($zeile = <IN>) {
  print $zeile;
}
close IN;
```
