I'm working on learning [leaflet.js](https://leafletjs.com/). 

Click below to see these live. I expect these will build on themselves.



## From zero to not-zero

[day 1](https://josh.works/leaflet_practice/01/index.html) (working through the beginner tutorial, customizing it a bit where possible/reasonable)
[day 2](https://josh.works/leaflet_practice/02/index.html) (more of the same)
[day 3](https://josh.works/leaflet_practice/03/index.html) (Mobile, "show current location" functionality)

### Notes for each day (newest on top)

#### Day 3

The [Leaflet mobile example](https://leafletjs.com/examples/mobile/) doesn't work super well.

I was getting 404s in the network tab with requests such as:

```
GET
	https://api.mapbox.com/styles/v1/mapbox/satellite-v9/tiles/-1/0/0?access_token=asdfasdf
```

I found this open GH issue: [404 in Mobile Example](https://github.com/Leaflet/Leaflet/issues/7528), someone suggested adding a `minZoom` attribute to the `L.titleLayer` request.

