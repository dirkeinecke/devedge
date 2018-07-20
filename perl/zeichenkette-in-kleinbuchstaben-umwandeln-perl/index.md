---
title: Zeichenkette in Kleinbuchstaben umwandeln
---

## Zeichenkette in Kleinbuchstaben umwandeln

### Beispiel #1 - gesamte Zeichenkette umwandeln

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

print "\L$text"; # Ausgabe: das ist ein text.
```

### Beipsiel #2 - Teil einer Zeichenkette umwandeln

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

print "\L$text\E Und das ist auch ein Text."; # Ausgabe: das ist ein text. Und das ist auch ein Text.
```
