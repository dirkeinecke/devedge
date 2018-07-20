---
title: Perl-Version ausgeben
---

## Perl-Version ausgeben

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

print $];
```

Die Ausgabe der Versionsnummer von Perl kann verschiedene Formate haben. Zum Beispiel:

- 1.2.3
- 1.2.3.0
- 1.002003
- 1.002003000

So ist zum Beispiel die Ausgabe von "5.008008" die Perl-Version 5.8.8.
