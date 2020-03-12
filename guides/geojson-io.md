# Geojson.io Guide

Guide to using [Geojson.io](http://geojson.io) - a super handy tool for inspecting and creating geojson (and other spatial formats) in the browser.


## Methods

### Importing data


### Making Data


### Sharing Data

Let's say you have a geojson that looks like this...

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
          -73.98738384246826,
          40.69422419919203
        ]
      }
    }
  ]
}
```

...and you want to share that data rendered on a map in geojson.io, you can do so by sharing the data in a number of ways. 

### as a URL

Part of the Geojson.io API allows us to create data and share it in a nice way. Let's say we have some data we created in geojson.io, e.g. like the point data we created above, what we can do if we want to share this data is:

* Step 1: encode that geojson into a URI encoded string (basically a long string that can be parsed by your browser's nav bar) → 

   | before    | → | after |
   |:----    | ---| ----- |
   |   `{"type":"FeatureCollection","features":{"type":"Feature","properties":{"color":"red"},"geometry":{"type":"Point","coordinates":[-73.98738384246826,40.69422419919203]}}]}`       |  `encodeURIComponent(JSON.stringify(myData))`  |  http://geojson.io/#data=data:application/json,%7B%22type%22%3A%22FeatureCollection%22%2C%22features%22%3A%5B%7B%22type%22%3A%22Feature%22%2C%22properties%22%3A%7B%22color%22%3A%22red%22%7D%2C%22geometry%22%3A%7B%22type%22%3A%22Point%22%2C%22coordinates%22%3A%5B-73.98738384246826%2C40.69422419919203%5D%7D%7D%5D%7D |

* Step 2: then append that long string at the end of the this `http://geojson.io/#data=data:application/json,` url so we can get a URL of our map and data we can share:
     ```txt
     http://geojson.io/#data=data:application/json,%7B%22type%22%3A%22FeatureCollection%22%2C%22features%22%3A%5B%7B%22type%22%3A%22Feature%22%2C%22properties%22%3A%7B%22color%22%3A%22red%22%7D%2C%22geometry%22%3A%7B%22type%22%3A%22Point%22%2C%22coordinates%22%3A%5B-73.98738384246826%2C40.69422419919203%5D%7D%7D%5D%7D
     ```

To acheive this, follow the steps below:

1. Step 1: open your browser's **dev tools**:
2. Step 2: store your current map data into a variable. Let's just call this `myData`. To do this, type into your **dev tool console**:
   ```js
   const myData = window.api.data.all().map;
   ```
   ![screenshot of the command to retrieve the data stored in the window.api.all().map object](../assets/images/geojsonio__share--01.png)
   ![screenshot of the geojson object that is stored in the window.api.data.all().map object](../assets/images/geojsonio__share--02.png)
3. Step 3: Turn your geojson data into a encoded URI string and append it to the end of the geojson.io url. To do this, type into your **dev tools console**:  
   ```js
   const mapUrl = `http://geojson.io/#data=data:application/json,${encodeURIComponent(JSON.stringify(myData))}`
   ```
   ![screenshot of the command and the url string that was produced](../assets/images/geojsonio__share--03.png)
4. Step 4: type `mapUrl` in the **dev tools console** to get back your data encoded in a nice way for geojson.io to render your data when navigating to that url:
     ```js
     "http://geojson.io/#data=data:application/json,%7B%22type%22%3A%22FeatureCollection%22%2C%22features%22%3A%5B%7B%22type%22%3A%22Feature%22%2C%22properties%22%3A%7B%22color%22%3A%22red%22%7D%2C%22geometry%22%3A%7B%22type%22%3A%22Point%22%2C%22coordinates%22%3A%5B-73.98738384246826%2C40.69422419919203%5D%7D%7D%5D%7D"
     ```
5. Step 5: Take everything between the quotations `" ... "` and paste that into another browser window navigation bar to see the super cool map!
  ![screenshot of geojson.io showing the data we created](../assets/images/geojsonio__share--05.png)





## References

* [Geojson.io URL API](https://github.com/mapbox/geojson.io/blob/gh-pages/API.md#url-api)
* [Geojson.io Console API](https://github.com/mapbox/geojson.io/blob/gh-pages/API.md#console-api)

