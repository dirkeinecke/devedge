---
title: UserLocation auf MKMapView ausblenden
---

## UserLocation auf MKMapView ausblenden

Das folgende Beispiel zeigt, wie man die UserLocation auf einer MKMapView ausblenden kann (aber trotzdem auf diese zugreifen kann). Es wird also nur der blaue Punkt ausgeblendet.

```objective_c
- (void)mapView:(MKMapView *)theMapView didAddAnnotationViews:(NSArray *)views {
  MKAnnotationView *ulv = [theMapView viewForAnnotation:theMapView.userLocation];
  ulv.hidden = YES;
}
```
