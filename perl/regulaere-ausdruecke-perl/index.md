---
title: Reguläre Ausdrücke
---

## Reguläre Ausdrücke

### Beispiel #1

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

if ($text =~ /ein/) { # sucht "ein"
  print 'Gefunden!';
} else {
  print "Nicht gefunden!";
}
```

### Beispiel #2

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

if ($text =~ /Text.$/) { # sucht "Text." am Ende ($)
  print 'Gefunden!';
} else {
  print "Nicht gefunden!";
}
```

### Beispiel #3

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

if ($text =~ /IsT/i) { # sucht "IsT" unabhängig von Klein- und Großschreibung (i)
  print 'Gefunden!';
} else {
  print "Nicht gefunden!";
}
```

### Beispiel #4

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Der / ist das Trennzeichen für Anfang und Ende.';

if ($text =~ /\//) { # sucht "/"; der / muss maskiert werden
  print 'Gefunden!';
} else {
  print "Nicht gefunden!";
}
```

### Beispiel #4 A

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Der / ist das Trennzeichen für Anfang und Ende.';

if ($text =~ m{/}) { # sucht "/" mit eigenen Tennzeichen (m)
  print 'Gefunden!';
} else {
  print "Nicht gefunden!";
}
```

### Beispiel #5

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$text = 'Das ist ein Text.';

if ($text =~ /ist|ein/) { # sucht "ist" oder (|) "ein"
  print 'Gefunden!';
} else {
  print "Nicht gefunden!";
}
```

### Siehe auch

- [Reguläre Ausdrücke in Ruby](../ruby/regulaere-ausdruecke-ruby)
- [Reguläre Ausdrücke in Python](../python/regulaere-ausdruecke)
