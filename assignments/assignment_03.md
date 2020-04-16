# A3: Web Mapping Practice

## Background 
Last week you explored web mapping with Kepler.gl - I hope you enjoyed it :)

This week, I would like to introduce 2 more tools:
* [DataWrapper.de](https://www.datawrapper.de/): DataWrapper is a tool for building graphics, often times for journalism. The team has spent a lot of time considering maps for public communication.
* [Leaflet.js](https://leafletjs.com/): Leaflet.js is a javascript library for building interactive web applications. You might say it is like the p5 of web mapping. 

This is inspired by [Lisa Charlotte Rost's - What I Learned Recreating One Chart Using 24 Tools](https://source.opennews.org/articles/what-i-learned-recreating-one-chart-using-24-tools/)

## The Challenge

Your challenge this week is create a choropleth map in each of the 3 tools. 

This exercise is designed to make you aware of map details such as...
* Map colors - using colorbrewer2
* Data “binning” (aka classification) 
* Map Information:
* Author, title, data cited, … 

...and to...
* Cue you into the advantages and disadvantages of different tools for geovisualization and mapping
* Propose a workflow for prototyping

## Step-by-step

* Step 1: Get the data
  * You can either use data that are relevant for your final projects (recommended)
  * OR use
  * [Reported NYC Rat Sightings Spring 2019](https://gist.githubusercontent.com/joeyklee/c301b832ed6ae0d5ccf5e5aa803894bb/raw/13c7c34d3b9f1aa9e3dd29269e77e1eaf11c9655/nyc__rat-counts-by-neighborhood__201903-201905.geojson) // see property `ratCounts` - what other data might you need in order to normalize or standardize these counts to a rate or proportion? 
* Step 2: Read 
  * [What to consider when creating choropleth maps](https://blog.datawrapper.de/choroplethmaps/)
  * [How to choose a color palette for a choropleth map](https://blog.datawrapper.de/how-to-choose-a-color-palette-for-choropleth-maps/)
  * [Different units, different patterns](https://blog.datawrapper.de/weekly-chart-europegrowth/)
* Step 3: Start with DataWrapper
  * Choropleth map: https://academy.datawrapper.de/article/115-how-to-import-data-choropleth-map
  * Optional: 
    * [Create a locator map](https://academy.datawrapper.de/article/161-how-to-create-a-locator-map)
    * [Create a proportional symbol map](https://academy.datawrapper.de/article/114-how-to-create-a-symbol-map-in-datawrapper)
* Step 4: Translate your DataWrapper map and settings a Kepler.gl map (as best as you can)
* Step 5: Learn about web mapping with JavaScript in Leaflet.js
  * [Leaflet.js Tutorial - Maptime Boston](https://maptimeboston.github.io/leaflet-intro/)
  * [Leaflet.js Tutorial - Geosandbox](https://joeyklee.github.io/geosandbox/)
* Step 6: Translate your DataWrapper map to Leaflet.js
* Step 7: Reflect on the experience and what you found


## References
* https://blog.datawrapper.de/weekly-chart-europegrowth/
* https://blog.datawrapper.de/choroplethmaps/
* https://www.vis4.net/blog/2011/12/choropleth-maps/ 


## Submission

↳ 💌 [Google Form Assignment Submission](https://forms.gle/1tAfHZXEejZDubHg9)

