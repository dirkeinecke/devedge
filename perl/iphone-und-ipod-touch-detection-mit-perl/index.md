---
title: iPhone und iPod touch Detection mit Perl
---

## iPhone und iPod touch Detection mit Perl

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$ua = $ENV{HTTP_USER_AGENT};

sub detect_iPhone
{
  if ($ua =~ /iPhone/ || $ua =~ /iPod/) {
    return true;
  } else {
    return false;
  }
}

if (&detect_iPhone() eq true) {
  print '<p style="font-size: 30px">This is an iPhone or iPod touch.</p>';
} else {
  print '<p style="font-size: 30px">This is not an iPhone or iPod touch.</p>';
}
```
