---
title: Reguläre Ausdrücke (Ruby)
---

## Reguläre Ausdrücke (Ruby)

### Beispiel #1

```ruby
#!/usr/bin/ruby

puts "Content-type: text/html\n\n"

text = 'Das ist ein Text.'

if text =~ /ein/ # sucht "ein"
  puts 'Gefunden!'
else
  puts 'Nicht gefunden!'
end
```

### Beispiel #2

```ruby
#!/usr/bin/ruby

puts "Content-type: text/html\n\n"

text = 'Das ist ein Text.'

if text =~ /Text.$/ # sucht "Text." am Ende ($)
  puts 'Gefunden!'
else
  puts 'Nicht gefunden!'
end
```

### Beispiel #3

```ruby
#!/usr/bin/ruby

puts "Content-type: text/html\n\n"

text = 'Das ist ein Text.'

if text =~ /IsT/i # sucht "IsT" unabhängig von Klein- und Großschreibung (i)
  puts 'Gefunden!'
else
  puts 'Nicht gefunden!'
end
```

### Beispiel #4

```ruby
#!/usr/bin/ruby

puts "Content-type: text/html\n\n"

text = 'Der / ist das Trennzeichen für Anfang und Ende.'

if text =~ /\// # sucht "/"; der / muss maskiert werden
  puts 'Gefunden!'
else
  puts 'Nicht gefunden!'
end
```

### Beispiel #5

```ruby
#!/usr/bin/ruby

puts "Content-type: text/html\n\n"

text = 'Das ist ein Text.'

if text =~ /ist|ein/ # sucht "ist" oder (|) "ein"
  puts 'Gefunden!'
else
  puts 'Nicht gefunden!'
end
```

### Siehe auch

- [Reguläre Ausdrücke in Perl](/perl/regulaere-ausdruecke-perl){:target="_blank"}
- [Reguläre Ausdrücke in Python](/python/regulaere-ausdruecke){:target="_blank"}
