---
title: iPad Detection mit Ruby
---

## iPad Detection mit Ruby

```ruby
#!/usr/bin/ruby
require 'cgi'

cgi = CGI.new("html4Tr")

puts "Content-type: text/html\n\n"

def ipad_detect
  case ENV['HTTP_USER_AGENT']
  when /(iPad)/i
    return true
  else
    return false
  end
end

case ipad_detect
when true
  puts '<p style="font-size: 30px">This is an iPad.</p>'
else
  puts '<p style="font-size: 30px">This is not an iPad.</p>'
end
```
