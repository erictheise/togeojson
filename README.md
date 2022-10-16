## toGeoJSON

This is a simple fork of [mapbox/togeojson](https://github.com/mapbox/togeojson). I use it to prepare data for an application that does not make use of `coordTimes` and to reduce filesize and complexity I've added a `-n=true` switch that outputs an empty array into the resulting GeoJSON.

Although I use `.gpx` traces exclusively I have modified the section dealing with `.kml` to generate the same output. It's only been casually tested.
 
Processing the largish GPX trace from [`test/data/osm.gpx`](./test/data)–
```
./togeojson test/data/osm.gpx > with.json
./togeojson -n=true test/data/osm.gpx > without.json
```
–we see an 18% size reduction.
```
-rw-r--r--  1 erictheise  staff   665K Oct 15 19:03 with.json
-rw-r--r--  1 erictheise  staff   562K Oct 15 19:03 without.json
```
