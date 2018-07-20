---
title: Zeichenkette in Grossbuchstaben umwandeln
---

## Zeichenkette in Grossbuchstaben umwandeln

### Beispiel #1 - gesamte Zeichzenkette umwandeln

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

print "\U$text"; # Ausgabe: DAS IST EIN TEXT.
```

### Beispiel #2 - Teil einer Zeichenkette umwandeln

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

print "\U$text\E Und das ist auch ein Text."; # Ausgabe: DAS IST EIN TEXT. Und das ist auch ein Text.
```
