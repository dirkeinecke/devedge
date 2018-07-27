---
title: iPhone und iPod touch Detection mit Ruby
---

## iPhone und iPod touch Detection mit Ruby

```ruby
#!/usr/bin/ruby
require 'cgi'

cgi = CGI.new("html4Tr")

puts "Content-type: text/html\n\n"

def iphone_detect
  case ENV['HTTP_USER_AGENT']
  when /(iPhone|iPod)/i
    return true
  else
    return false
  end
end

case iphone_detect
when true
  puts '<p style="font-size: 30px">This is an iPhone or iPod touch.</p>'
else
  puts '<p style="font-size: 30px">This is not an iPhone or iPod touch.</p>'
end
```
