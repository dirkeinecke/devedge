---
title: URLs, Benutzernamen und Hash-Tags eines Tweets automatisch verlinken
---

## URLs, Benutzernamen und Hash-Tags eines Tweets automatisch verlinken

### Funktion

```php
<?php
  function tweet_auto_link($str_tweet) {
    $str_tweet = preg_replace("#(^|[\n ])([\w]+?://[\w]+[^ \"\n\r\t< ]*)#", '\\1<a href="\\2" target="_blank">\\2</a>', $str_tweet);
    $str_tweet = preg_replace("#(^|[\n ])((www|ftp)\.[^ \"\t\n\r< ]*)#", '\\1<a href="http://\\2" target="_blank">\\2</a>', $str_tweet);
    $str_tweet = preg_replace("/@(\w+)/", '<a href="http://www.twitter.com/\\1" target="_blank">@\\1</a>', $str_tweet);
    $str_tweet = preg_replace("/#(\w+)/", '<a href="http://search.twitter.com/search?q=\\1" target="_blank">#\\1</a>', $str_tweet);
    return $str_tweet;
  }
?>
```

### Beispiel

```php
<?php
  $str_tweet = 'Das ist ein #Test an @dirkeinecke';
  echo tweet_auto_link($str_tweet);
?>
```
