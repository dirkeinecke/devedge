---
title: Zahl auf beliebige Anzahl an Nachkommstellen runden (Ruby)
---

## Zahl auf beliebige Anzahl an Nachkommstellen runden (Ruby)

Ruby besitzt keine Methode, um eine Zahl vom Typ Float auf eine beliebige Anzahl an Nachkommastellen zu runden. Aus diesem Grund erweitere ich die Klasse `Float` um die Methode `round_to`. Dieser Methode kann die Anzahl der gewünschten Nachkommastellen übergeben werden.

```ruby
#!/usr/bin/ruby

puts "Content-type: text/html\n\n"

class Float
  def round_to(i)
    f = (10 ** i).to_f
    nr = self * f
    return nr.round / f
  end
end

value = 123.456
puts value.round_to(2) # Ausgabe: 123.46
```
