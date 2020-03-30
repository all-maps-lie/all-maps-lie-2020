# A2: Map Mashups

- [A2: Map Mashups](#a2-map-mashups)
  - [READINGS](#readings)
  - [BRIEF](#brief)
  - [TECHNICAL REFERENCES](#technical-references)
  - [Requirements](#requirements)
    - [Part 1: Continue data collection & research](#part-1-continue-data-collection--research)
    - [Part 2: Export your Streetview Mapper Data](#part-2-export-your-streetview-mapper-data)
    - [Part 3: Create a web map of your streetview locations](#part-3-create-a-web-map-of-your-streetview-locations)
    - [Part 4: Add data and interactivity to your map](#part-4-add-data-and-interactivity-to-your-map)
    - [Part 5: Deploy your map to Glitch:](#part-5-deploy-your-map-to-glitch)
    - [Part 6: Documentation & Organization](#part-6-documentation--organization)
  - [Submission](#submission)

## READINGS

* See [Week 2 Readings](../BIBLIOGRAPHY.md#week-02-countermaps--cartographics)

## BRIEF

This week your assignment is to create a web map of the data you collected in you one week of data collection (see: [Assignment #1](assignments/assignment_01.md)).

The point here is to explore the web mapping libraries [Leaflet.js](https://leafletjs.com/) and [MapboxGL.js](https://docs.mapbox.com/mapbox-gl-js/api/) using the [GeoSandbox](https://joeyklee.github.io/geosandbox/) and to get feeling for how you can write JavaScript code to put your data "on the map."

You are more than welcome to try using [Kepler.gl](https://kepler.gl/) to explore your data.

## TECHNICAL REFERENCES

* [Technical References](../BIBLIOGRAPHY.md#technical-references)

## Requirements

### Part 1: Continue data collection & research

Continue your **data collection** and **research** you started last week, this should occur in parallel with your web mapping exercises this week.

### Part 2: Export your Streetview Mapper Data

If you have not already done so, do [Assignment 1, Part 3](assignments/assignment_01.md#part-3-export-a-geojson-of-your-findings-and-plot-them-on-a-map). If you have continued your data collection, you can export the latest dataset so you have all the data you've collected thus far.

### Part 3: Create a web map of your streetview locations

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

### Part 4: Add data and interactivity to your map

Now that you have your map, you will:
* add your data to the map and 
* add some interactivity to your data. 

In this step you will:
1. Add data: Add your `.geojson` data as a layer on your the map.
2. Add interactivity: For each point add a popup that will show the image that was taken in that location. You will write a loop that will attach the [popup to each marker](https://leafletjs.com/reference-1.6.0.html#popup).

Pat yourself on the back! This mapping stuff can be challenging!

### Part 5: Deploy your map to Glitch:

Deploy your map to Glitch. 

* If you're using Git/Github, great! You can deploy to glitch by [following these instructions](https://github.com/itp-dwd/2020-spring/blob/master/guides/glitch.md)
* If you're not using Git/Github, you can simply upload your files using the file uploader. Once you make a blank project in glitch you can use the sidebar to **upload a file** with your `index.html` and other javascript and css files.


### Part 6: Documentation & Organization

Document your process, you understanding or questions about the code, and begin remarking on any patterns you might see when viewing your data on the map. Document this on your blog.

As part of your week 2 documentation you will submit the following:
1. A blog post that:
   1. **Provides a clear update about your data collection and research activities**: "e.g. This week, I continued my data collection of street trees. Since last Monday, I have collected an addtional 40 trees. I have started to identify some trends and patterns based on the data I've collected so far. So far, I have noticed: ... In reading the literature on urban vegetation, I've found that street tree health is related to many factors such as availablity of water which on a microscale can be influenced by the building density and materials of the buildings surrounding the tree... Street trees provide many benefits according to research published in X..."
   2. **Provides the link to your published web map**: In your blog post you will provide screenshots of your web map describing what you did to produce the map. You will provide references to code you used and/or any additional materials of relevance. e.g. "Here is a web map I produced using the tutorial provided here..."
   3. **Provides at least 3 points of reflection on the usage of open source mapping tools**: Provide some feedback about why open source mapping tools may or may not be important or relevant for research.

## Submission

You will submit a link to your blog post to the link below, specifying which assignment you are submitting:

↳ 💌 [Google Form Assignment Submission](https://forms.gle/1tAfHZXEejZDubHg9)


<!-- * Using your collected data:
  * Intro to web maps / geosandbox , data collection continued ==> points on a map, popups, images on the map -->

<!-- 
* Map Mashups: Intro to web maps / geosandbox , data collection continued ==> points on a map, popups, images on the map
 -->