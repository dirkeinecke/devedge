---
title: Belegter Webspace ermitteln (Ruby)
---

## Belegter Webspace ermitteln (Ruby)

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

webspace = 0
basicFolder = ENV['DOCUMENT_ROOT']
Dir.chdir(basicFolder)
Dir['**/*'].each do |filename|
  webspace = webspace.to_f + File.stat(filename).size # in Byte
end

if webspace >= 1099511627776
  puts (webspace/1099511627776).round_to(2).to_s + ' TB'
elsif webspace >= 1073741824
  puts (webspace/1073741824).round_to(2).to_s + ' GB'
elsif webspace >= 1048576
  puts (webspace/1048576).round_to(2).to_s + ' MB'
elsif webspace >= 1024
  puts (webspace/1024).round_to(2).to_s + ' KB'
else
  puts webspace.round_to(2).to_s + ' B'
end
```
