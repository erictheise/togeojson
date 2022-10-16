## toGeoJSON

This is a simple fork of [mapbox/togeojson](https://github.com/mapbox/togeojson). I use it to prepare data for an application that does not make use of `coordTimes` and to reduce filesize and complexity I've added a `-n=true` switch that outputs an empty array into the resulting GeoJSON.

Although I use `.gpx` traces exclusively I have modified the section dealing with `.kml` to generate the same output. It's only been casually tested.
 
