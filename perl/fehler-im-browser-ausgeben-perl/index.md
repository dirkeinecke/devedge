---
title: Fehler im Browser ausgeben
---

## Fehler im Browser ausgeben

```perl
#!/usr/local/bin/perl

use CGI::Carp 'fatalsToBrowser'; # Fehler sollen im Browser ausgegeben werden

print "Content-type: text/html\n\n";

print "Hallo Welt" # Hier fehlt das ; am Zeilenende
print "foo bar";
```

Ausgabe im Browser:

```
Software error:

syntax error at Fehler-im-Browser-ausgeben.pl line 8, near "print"
Execution of Fehler-im-Browser-ausgeben.pl aborted due to compilation errors.
For help, please send mail to the webmaster (webmaster@www.domain.de), giving this error message and the time and date of the error.
```
