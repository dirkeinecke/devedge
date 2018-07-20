---
title: Hash
---

## Hash

### Beispiel #1

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

%text = (wert1 => "Hallo", wert2 => "Welt");

print $text{wert1};
print " ";
print $text{wert2};
```

### Beispiel #2

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

%text = ();
$text{wert1} = "Hallo";
$text{wert2} = "Welt";

print $text{wert1};
print " ";
print $text{wert2};
```

### Beispiel #3

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

%text = ("wert1", "Hallo", "wert2", "Welt");

print $text{wert1};
print " ";
print $text{wert2};
```
