---
title: Datei schreiben
---

## Datei schreiben

```perl
#!/usr/local/bin/perl

use CGI::Carp 'fatalsToBrowser'; # Fehler sollen im Browser ausgegeben werden

print "Content-type: text/html\n\n";

$datei = 'testdatei.txt';
$inhalt = 'Das ist ein Text.';

open OUT, "> $datei" or die "Kann $datei nicht zum Schreiben oeffnen: $!";
print OUT $inhalt;
close OUT or die "Kann $datei nicht schliessen: $!";
```
