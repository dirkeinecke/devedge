---
title: Kilometer in Meilen umrechnen
---

## Kilometer in Meilen umrechnen

```javascript
convert_km_to_miles = function(km, decimal_place) {
  miles = parseInt(km) * 0.621371;

  if (decimal_place != -1) {
    var a = Math.pow(10, decimal_place);
    miles = Math.round(miles * a) / a;
  }

  return miles;
}

miles = convert_km_to_miles(100, 2);
```
