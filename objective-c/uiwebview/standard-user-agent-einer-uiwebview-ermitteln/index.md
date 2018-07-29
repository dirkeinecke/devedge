---
title: Standard User-Agent einer UIWebView ermitteln
---

## Standard User-Agent einer UIWebView ermitteln

Das folgende Beispiel zeigt, wie man den Standard User-Agent einer `UIWebView` ermitteln kann.

```objective_c
UIWebView *webView = [[UIWebView alloc] initWithFrame:CGRectZero];
NSString *userAgent = [webView stringByEvaluatingJavaScriptFromString:@"navigator.userAgent"];
```
