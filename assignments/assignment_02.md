# A2: Map Mashups

## Brief:

This week your assignment is to create a web map of the data you collected in you one week of data collection (see: [Assignment #1](./assignment_01.md)).

The point here is to explore the web mapping libraries [Leaflet.js](https://leafletjs.com/) and [MapboxGL.js](https://docs.mapbox.com/mapbox-gl-js/api/) using the [GeoSandbox](https://joeyklee.github.io/geosandbox/) and to get feeling for how you can write JavaScript code to put your data "on the map."

You are more than welcome to try using [Kepler.gl](https://kepler.gl/) to explore your data.

## Readings

* See [Week 2 Readings](../BIBLIOGRAPHY.md#week-02-countermaps--cartographics)

## Technical References

* [Technical References](../BIBLIOGRAPHY.md#technical-references)

## Requirements

### Part 0: Create data from your images

If you have not already done so, create a `.geojson` file that includes the EXIF metadata from your images. You can use the [img2meta]() tool to do this.

As a quick test, drag-and-drop your `.geojson` file onto [Geojson.io](http://geojson.io/) to see if your data creation was successful. 

📸 Take a screenshot as documentation.

### Part 1: Create a web map of your photographed locations

Create a web map. Your web map will include the following elements:
1. [Scalebar](https://leafletjs.com/reference-1.6.0.html#control-scale)
2. [Zoom Controls](https://leafletjs.com/reference-1.6.0.html#control-zoom)
3. [Attribution](https://leafletjs.com/reference-1.6.0.html#control-zoom)
4. Information about your map:
   * About the map:
     * [ ] the data collection methods
     * [ ] the author -- you!
     * [ ] the date of creation
     * [ ] the date the map was last updated
   * Where to inlcude:
     * [ ] You can include this in the body of your HTML or you can use the [Leaflet Sidebar V2](https://github.com/nickpeihl/leaflet-sidebar-v2/) for a nice and responsive UI element on your map.

### Part 2: Add data and interactivity to your map

Now that you have your map, you will:
* add your data to the map and 
* add some interactivity to your data. 

In this step you will:
1. Add data: Add your `.geojson` data as a layer on your the map.
2. Add interactivity: For each point add a popup that will show the image that was taken in that location. You will write a loop that will attach the [popup to each marker](https://leafletjs.com/reference-1.6.0.html#popup).


### Part 3: Documentation & Organization

Pat yourself on the back! This mapping stuff can be challenging!

Document your process, you understanding or questions about the code, and begin remarking on any patterns you might see when viewing your data on the map. Document this on your blog.

* Key questions:
  * ...
  * ...
  * ...

## Submission

↳ 💌 [Google Form Assignment Submission](https://forms.gle/1tAfHZXEejZDubHg9)


<!-- * Using your collected data:
  * Intro to web maps / geosandbox , data collection continued ==> points on a map, popups, images on the map -->

<!-- 
* Map Mashups: Intro to web maps / geosandbox , data collection continued ==> points on a map, popups, images on the map
 -->