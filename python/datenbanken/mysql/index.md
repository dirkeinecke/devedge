---
title: MySQL
---

## MySQL

### Beispiel #1 - Verbindung zu einem Datenbankserver herstellen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import MySQLdb

print "Content-type: text/plain\n\n"

connection = MySQLdb.connect("localhost", "Benutzername", "Kennwort", "Datenbankname")
```

### Beispiel #2 - Tabelle anlegen

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import MySQLdb

print "Content-type: text/plain\n\n"

connection = MySQLdb.connect("localhost", "Benutzername", "Kennwort", "Datenbankname")

cursor = connection.cursor()
cursor.execute("CREATE TABLE personen (vorname TEXT, nachname TEXT, geburtsjahr INTEGER)")
```

### Beispiel #3 - einen Datensatz speichern

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import MySQLdb

print "Content-type: text/plain\n\n"

connection = MySQLdb.connect("localhost", "Benutzername", "Kennwort", "Datenbankname")

cursor = connection.cursor()
cursor.execute("INSERT INTO personen VALUES ('Max', 'Mustermann', 1979)")
```

### Beispiel #4 - mehrere Datensätze speichern

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import MySQLdb

print "Content-type: text/plain\n\n"

connection = MySQLdb.connect("localhost", "Benutzername", "Kennwort", "Datenbankname")
cursor = connection.cursor()

personen = ( ('Max', 'Mustermann', 1979), ('Susi', 'Sorglos', 1998) )
cursor.executemany("INSERT INTO personen VALUES (%s, %s, %s)", personen)
```

### Beispiel #5 - alle Datensätze auslesen und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import MySQLdb

print "Content-type: text/plain\n\n"

connection = MySQLdb.connect("localhost", "Benutzername", "Kennwort", "Datenbankname")
cursor = connection.cursor()

cursor.execute("SELECT vorname, nachname, geburtsjahr FROM personen")

for row in cursor:
  print "%s %s (%d)" % row

# Ausgabe:
#
# Max Mustermann (1979)
# Susi Sorglos (1998)
```

### Beispiel #6 - bestimmte Datensätze auslesen und ausgeben

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import MySQLdb

print "Content-type: text/plain\n\n"

connection = MySQLdb.connect("localhost", "Benutzername", "Kennwort", "Datenbankname")
cursor = connection.cursor()

cursor.execute("SELECT geburtsjahr FROM personen WHERE vorname=%s AND nachname=%s", ('Max', 'Mustermann'))

for row in cursor:
  print "%d" % row # Ausgabe: 1979
```
