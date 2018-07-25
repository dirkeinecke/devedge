---
title: RSS-Reader
---

## RSS-Reader

### Hinweis

- Dies ist nur ein einfaches Grundgerüst für einen RSS-Reader.
- Dieses Grundgerüst ist (noch) nicht für den produktiven Einsatz ausgelegt.

```python
#!/usr/bin/env python
# -*- coding: utf8 -*-

import urllib2
import xml.dom.minidom as dom
from email.utils import parsedate
from time import strftime

print "Content-type: text/html\n\n"

class rssFeed(object):

  __slots__ = ("__url", "__items")

  def __init__(self, url):
    self.__url = url
    self.__items = []

  def __del__(self):
    pass

  def __getNodeText(self, node):
    text = ''

    # Nur wenn es kein leerer Knoten ist
    # (Beispiel: <link></link>, <link/>)
    if node.hasChildNodes() == True:
      return node.firstChild.data.strip().encode('utf8')

    return text

  def loadItems(self):
    f = urllib2.urlopen(self.__url)
    content = f.read()
    xml = dom.parseString(content)
    itemNodes = xml.getElementsByTagName('item')

    for item in itemNodes:
      title = ''          # Knoten <title> ist optional für <item>
      description = ''    # Knoten <description> ist optional für <item>
      link = ''           # Knoten <link> ist optional für <item>
      pubDate = ''        # Knoten <pubDate> ist optional für <item>
      for node in item.childNodes:
        if node.nodeName == "title":
          title = self.__getNodeText(node)
        elif node.nodeName == "description":
          description = self.__getNodeText(node)
        elif node.nodeName == "link":
          link = self.__getNodeText(node)
        elif node.nodeName == "pubDate":
          pubDate = self.__getNodeText(node)
          pubDate = parsedate(pubDate) # Tuple
          pubDate = strftime("%d.%m.%Y %H:%M:%S", pubDate)

      obj = rssFeedItem(title, description, link, pubDate)
      self.__items.append(obj)

  # Setter

  def __setUrl(self, url):
    self.__url = url
        
  # Getter
    
  def __getUrl(self):
    return self.__url

  def __getItems(self):
    return self.__items

  url = property(__getUrl, __setUrl)
  items = property(__getItems)

class rssFeedItem(object):

  __slots__ = ("__title", "__description", "__link", "__pubDate")

  def __init__(self, title, description, link, pubDate):
    self.__title = title
    self.__description = description
    self.__link = link
    self.__pubDate = pubDate

  def __del__(self):
    pass

  # Setter
    
  def __setTitle(self, title):
    self.__title = title

  def __setDescription(self, description):
    self.__description = description
        
  def __setLink(self, link):
    self.__link = link

  def __setPubDate(self, pubDate):
    self.__pubDate = pubDate

  # Getter

  def __getTitle(self):
    return self.__title

  def __getDescription(self):
    return self.__description

  def __getLink(self):
    return self.__link

  def __getPubDate(self):
    return self.__pubDate

  title = property(__getTitle, __setTitle)
  description = property(__getDescription, __setDescription)
  link = property(__getLink, __setLink)
  pubDate = property(__getPubDate, __setPubDate)

# Beispiel-RSS-Feed:
#url = 'http://www.global-talk.org/external.php?type=RSS2'
#url = 'http://www.all-okay.de/?feed=rss2'
#url = 'http://www.avm.de/de/Extern/RSS/rss.xml'
url = 'http://www.spiegel.de/schlagzeilen/tops/index.rss'

rssFeed1 = rssFeed(url)
rssFeed1.loadItems()

out = ''
out += '<ul>'
for item in rssFeed1.items:
  out += '<li>'
  if item.link != '':
    out += '<a href="' + item.link + '" target="_blank">'
  out += item.title
  if item.link != '':
    out += '</a>'
  if item.pubDate != '':
    out += '<br>'
    out += '<small>' + item.pubDate + ' Uhr</small>'
  out += '<br><br>'
  out += item.description
  out += '<br><br>'
  out += '</li>'
out += '</ul>'

print out
```
