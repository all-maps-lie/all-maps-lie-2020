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

* **header row**: you'll want to make sure that your data has a header row, e.g. the column names. The best practice for column names are:
  * no spaces - use underscores (`_`) or camel case
  * no weird characters - just numbers and letters
  * for spatial CSV, you'll want to have a columns called **latitude** and **longitude** with the relevant values as floating point numbers.
* **Make sure your data is formatted properly**: If you're using or creating CSV data, quite likely you're using some kind of spreadsheet program like Google Sheets, Numbers, Excel, or Open Office. If not, you're probably then getting outputs from some program or just using your text editor. Regardless, you'll probably want some way to make sure your CSV data is structured properly. You can run your data through a linter that will check to see if your data are properly formatted: 
  * [CSV Lint](https://csvlint.io/)

Once your data is ready to go, it's time to convert it!


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