I'm working on learning [leaflet.js](https://leafletjs.com/). 

Click below to see these live. I expect these will build on themselves.



## From zero to not-zero

- [day 1](https://josh.works/leaflet_practice/01) (working through the beginner tutorial, customizing it a bit where possible/reasonable)
- [day 2](https://josh.works/leaflet_practice/02) (more of the same)
- [day 3](https://josh.works/leaflet_practice/03) (Mobile, "show current location" && zoom to current location functionality)
- [day 4](https://josh.works/leaflet_practice/04) (Custom markers)

### Notes for each day (newest on top)

#### Day 4 - custom markers

Getting icons from [https://thenounproject.com/](https://thenounproject.com/). I'm going to add markers to a map in Golden to represent (for example) various sorts of mobility problems, like:

- Spots where people in wheelchairs would be at risk
- Spots where people in cars and people on bikes are at risk of collision
- Spots where people in cars and people walking are at risk of collision
- spots where people on bikes and people walking are at risk of collision
- spots where people walking would be unhappy

#### Day 3 - show current location (mobile and desktop)

The [Leaflet mobile example](https://leafletjs.com/examples/mobile/) doesn't work super well.

I was getting 404s in the network tab with requests such as:

```
GET
	https://api.mapbox.com/styles/v1/mapbox/satellite-v9/tiles/-1/0/0?access_token=asdf
```

I found this open GH issue: [404 in Mobile Example](https://github.com/Leaflet/Leaflet/issues/7528), someone suggested adding a `minZoom: -1` attribute to the `L.titleLayer` request.

Makes sense, because inspecting the same `get` in a functioning example was returning something like:

```
GET 
  https://api.mapbox.com/styles/v1/mapbox/satellite-v9/tiles/0/0/0?access_token=asdf
```

I wish they'd fix the example.

## Ideas 

- reimplement a local version of [shadowmapper](https://github.com/perliedman/shadow-mapper) (intro blog post)[http://www.liedman.net/2014/06/25/sunshine/]
