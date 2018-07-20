---
title: iPad Detection mit Perl
---

## iPad Detection mit Perl

```perl
#!/usr/local/bin/perl

print "Content-type: text/html\n\n";

$ua = $ENV{HTTP_USER_AGENT};

sub detect_iPad
{
  if ($ua =~ /iPad/) {
    return true;
  } else {
    return false;
  }
}

if (&detect_iPad() eq true) {
  print '<p style="font-size: 30px">This is an iPad.</p>';
} else {
  print '<p style="font-size: 30px">This is not an iPad.</p>';
}
```
