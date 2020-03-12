# Converting a CSV to GeoJSON

## Overview

Convert a CSV file that looks like this: **my-data.csv**
```csv
"latitude","longitude","color"
0,0,"red"
```
to a geojson that looks like this: **my-data.geojson**
```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "color": "red"
      },
      "geometry": {
        "type": "Point",
        "coordinates": [
          0,
          0
        ]
      }
    }
  ]
```


## Prep your data




## Convert your data!

First choice:
* 🌟[Geojson.io](http://geojson.io) // you can open a CSV file directly in geojson.io and it will generate a geojson file for you. You must have a header row with fields called "latitude" and "longitude" or "lat" and "lon". Make sure any null values are accounted for. - This would probably be my go-to option.
  * NOTE: the development of Geojson.io as of late has been suspended, but it still works great, however if things seem funky, there's a new fork of the project called [geojson.net](https://geojson.net/#2/20.0/0.0). 

Other options:
* [Csv2GeoJSON - Mapbox](https://github.com/mapbox/csv2geojson) // if you're into command line tools, you can download and install Mapbox's handy csv2geojson tool. Having this installed could be nice if you anticipate doing this more frequently!
* [CSV.togeojson tool](http://csv.togeojson.com/) // One of the many tools for converting your a csv file to geojson. Nothing fancy going on here besides parsing your file and a structuring it in geojson format.

## References:

* [Geojson.io](http://geojson.io)
* [Csv2GeoJSON - Mapbox](https://github.com/mapbox/csv2geojson)
* [CSV.togeojson tool](http://csv.togeojson.com/)