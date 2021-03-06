---
title: if-Anweisung
---

## if-Anweisung

*Inhalt*

- [Beispiel #1 - numerische Gleichheit](#beispiel-1---numerische-gleichheit)
- [Beispiel #2 - numerische Ungleichheit](#beispiel-2---numerische-ungleichheit)
- [Beispiel #3 - Gleichheit von Zeichenketten](#beispiel-3---gleichheit-von-zeichenketten)
- [Beispiel #4 - Ungleichheit von Zeichenketten](#beispiel-4---ungleichheit-von-zeichenketten)
- [Beispiel #5 - numerisch kleiner als](#beispiel-5---numerisch-kleiner-als)
- [Beispiel #6 - numerisch größer als](#beispiel-6---numerisch-größer-als)
- [Beispiel #7 - kleiner als bei Zeichenketten](#beispiel-7---kleiner-als-bei-zeichenketten)
- [Beispiel #8 - größer als bei Zeichenketten](#beispiel-8---größer-als-bei-zeichenketten)
- [Beispiel #9 - numerisch kleiner/gleich](#beispiel-9---numerisch-kleinergleich)
- [Beispiel #10 - numerisch größer/gleich](#beispiel-10---numerisch-größergleich)
- [Beispiel #11 - kleiner/gleich bei Zeichenketten](#beispiel-11---kleinergleich-bei-zeichenketten)
- [Beispiel #12 - größer/gleich bei Zeichenketten](#beispiel-12---größergleich-bei-zeichenketten)
- [Weitere logische Operatoren](#weitere-logische-operatoren)

### Beispiel #1 - numerische Gleichheit

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if (1 == 2) {
  print "1 ist 2";
} else {
  print "1 ist nicht 2";
}
```

### Beispiel #2 - numerische Ungleichheit

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if (1 != 2) {
  print "1 ist nicht 2";
} else {
  print "1 ist 2";
}
```

### Beispiel #3 - Gleichheit von Zeichenketten

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if ('Hallo' eq 'Welt') {
  print 'Hallo ist Welt';
} else {
  print "Hallo ist nicht Welt";
}
```

### Beispiel #4 - Ungleichheit von Zeichenketten

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if ('Hallo' ne 'Welt') {
  print 'Hallo ist nicht Welt';
} else {
  print "Hallo ist Welt";
}
```

### Beispiel #5 - numerisch kleiner als

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if (1 < 2) {
  print '1 ist kleiner als 2';
} else {
  print "1 ist nicht kleiner als 2";
}
```

### Beispiel #6 - numerisch größer als

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if (2 > 1) {
  print '2 ist groesser als 1';
} else {
  print '2 ist nicht groesser als 1';
}
```

### Beispiel #7 - kleiner als bei Zeichenketten

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if ('a' lt 'b') {
  print 'a ist kleiner als b';
} else {
  print 'a ist nicht kleiner als b';
}
```

### Beispiel #8 - größer als bei Zeichenketten

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if ('b' gt 'a') {
  print 'b ist groesser als a';
} else {
  print 'b ist nicht groesser als a';
}
```

### Beispiel #9 - numerisch kleiner/gleich

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if (1 <= 1) {
  print '1 ist kleiner/gleich 1';
} else {
  print '1 ist nicht kleiner/gleich 1';
}
```

### Beispiel #10 - numerisch größer/gleich

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if (2 >= 1) {
  print '2 ist groesser/gleich 1';
} else {
  print '2 ist nicht groesser/gleich 1';
}
```

### Beispiel #11 - kleiner/gleich bei Zeichenketten

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if ('a' le 'b') {
  print 'a ist kleiner/gleich b';
} else {
  print 'a ist nicht kleiner/gleich b';
}
```

### Beispiel #12 - größer/gleich bei Zeichenketten

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

if ('b' ge 'a') {
  print 'b ist groesser/gleich a';
} else {
  print 'b ist nicht groesser/gleich a';
}
```

### Weitere logische Operatoren

- `and`
- `or`
- `not`
