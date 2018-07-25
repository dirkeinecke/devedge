---
title: Template-System des Moduls string
---

## Template-System des Moduls string

### Beispiel #1

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from string import Template

print "Content-type: text/plain\n\n"

t = Template("Mein Name ist $vorname $nachname.")

print t.substitute(vorname="Max", nachname="Mustermann") # Ausgabe: Mein Name ist Max Mustermann.
print t.substitute(nachname="Mustermann", vorname="Max") # Ausgabe: Mein Name ist Max Mustermann.
```

### Beispiel #2 - Werte für Platzhalter als Dictionary übergeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from string import Template

print "Content-type: text/plain\n\n"

t = Template("Mein Name ist $vorname $nachname.")
werte = {"vorname": "Max", "nachname": "Mustermann"}

print t.substitute(werte) # Ausgabe: Mein Name ist Max Mustermann.
```

### Beispiel #3 - weniger Werte als Platzhalter

Werden der Methode `substitude()` weniger Parameter übergeben als Platzhalter in der Vorlage (Template) vorhanden sind, dann wird eine KeyError-Exeption geworfen. Dies kann man umgehen, indem man die Methode `save_substitude()` verwendet.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from string import Template

print "Content-type: text/plain\n\n"

t = Template("Mein Name ist $vorname $nachname.")

print t.safe_substitute(vorname="Max") # Ausgabe: Mein Name ist Max $nachname.
```

### Beispiel #4 - Name des Platzhalters in geschweiften Klammern

Folgt gleich im Anschluß auf den Namen des Platzhalters weiterer Text, muss der Name des Platzhalters in geschweifte Klammern gesetzt werden.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from string import Template

print "Content-type: text/plain\n\n"

t = Template("${anzahl}mal")

print t.substitute(anzahl="5") # Ausgabe: 5mal
```

### Beispiel #5 - Dollar-Zeichen in der Vorlage (Template)

Möchte man das Dollar-Zeichen unabhängig von den Platzhaltern in einer Vorlage (Template) verwenden, dann muss man dafür zwei Dollar-Zeichen schreiben.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

from string import Template

print "Content-type: text/plain\n\n"

t = Template("Der Preis sollte $$$preis nicht übersteigen.")

print t.substitute(preis="100") # Ausgabe: Der Preis sollte $100 nicht übersteigen.
```
