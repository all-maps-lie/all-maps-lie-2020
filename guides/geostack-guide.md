---
created_date: 2020-04-12
updated_date: 2020-04-12
---

# Geostack Guide

This is a list of tools that either I use regularly or can recommend based on experience or evaluated potential. This focuses mostly on mapping platforms, software, and tools, but I might throw in a few curve balls here and there. There's certainly a lot of other workflows and setups, but hopefully this is useful.


- [Geostack Guide](#geostack-guide)
  - [Quickstart](#quickstart)
    - [Get started with (Geo)Data & Geovisualization](#get-started-with-geodata--geovisualization)
    - [JavaScript & Web Mapping](#javascript--web-mapping)
    - [Desktop GIS](#desktop-gis)
  - [Desktop GIS](#desktop-gis-1)
  - [Frontend](#frontend)
    - [JavaScript Web Mapping Libraries](#javascript-web-mapping-libraries)
    - [JavaScript Charting Libraries](#javascript-charting-libraries)
    - [Refinement](#refinement)
  - [Backend](#backend)
    - [Server](#server)
    - [Geodatabases](#geodatabases)
  - [Technical References](#technical-references)
  - [References](#references)

***
***
***

## Quickstart

### Get started with (Geo)Data & Geovisualization

* **Step 1**: Start with a spreadsheet software and get an understanding of data and questions that might be asked with data
  * Excel or google spreadsheets (believe it or not!) - [Spreadsheets tutorial by the NYT](https://open.nytimes.com/how-we-helped-our-reporters-learn-to-love-spreadsheets-adc43a93b919)
* **Step 2**: Explore mapping possibilities using a full featured mapping platform designed for journalism and publication 
  * [DataWrapper](https://www.datawrapper.de/) - nice interface for exploring data and making visualizations quickly. 
* **Step 3**: Explore your data in a more interactive, slippy web map context 
  * [Kepler.gl](https://kepler.gl/) - snappy interface running on mapboxgl with really nice exporting functions 

### JavaScript & Web Mapping
* Leaflet.js:
  * [Maptime Boston Leaflet.js Intro](https://maptimeboston.github.io/leaflet-intro/)
  * [GeoSandbox Tutorial - Leaflet.js](https://joeyklee.github.io/geosandbox/hello-leaflet.html)
  * [Leaflet.js Starter](https://github.com/joeyklee/leafletjs-starter)

### Desktop GIS
* [QGIS](https://www.qgis.org/en/site/) - Quantum GIS, open source GIS program. Lots of plugins to do complex analyses and even create web maps!

***
***
***

## Desktop GIS
* [QGIS](https://www.qgis.org/en/site/)

## Frontend

The frontend is comprised of...most of those things that you'd only use once you've completed your data processing and analysis. These are the things you're using to either create interactive applications to collect data and/or publish your analyses.

### JavaScript Web Mapping Libraries

* Slippy Web Mapping Visualization Libraries
  * [Leaflet.js](https://leafletjs.com/) - my preference is leaflet.js over mapboxgl mostly because I think the documentation is more approachable and a bit easier to bend to your will.
  * [MapboxGL.js](https://docs.mapbox.com/mapbox-gl-js/overview/) - super powerful and snappy, but the GL aspect of it all can sometimes feel tricky.
* Vector Mapping on the Web 
  * [D3.js](https://d3js.org/) - for mapping and visualization outside of the web mercator. [Check out the geo projections in D3.js](https://github.com/d3/d3-geo-projection/) // probably can't beat d3's projection library

### JavaScript Charting Libraries
Because maps don't always live by themselves...

* [ChartJS](https://www.chartjs.org/) // friendly canvas based rendering
* [Plotly - JavaScript](https://plot.ly/javascript/) // svg based rendering
* [RawGraphs](https://rawgraphs.io/) // nice user interface for exploring data and making visualizations quickly.

### Refinement

* Sketch App for Mac: For working with PDFs and SVGs for refining maps

***
***
***

## Backend

The backend is comprised of...

### Server

* [Node.js](https://nodejs.org/en/) - Serverside JavaScript
  * Geoprocessing:
    * [Turf.js](https://turfjs.org/) - Turfjs for running on the server or browser in JavaScript
    * [GDAL for Node.js](https://www.npmjs.com/package/gdal)
  * Web Server:
    * [Express.js](https://www.npmjs.com/package/express)
    * [Tilehut.js](https://github.com/b-g/tilehut) - if you need to serve up and host your own raster and vector tiles. Pairs will with [Tippecanoe - Generate Vector Tiles from GeoJSON](https://github.com/mapbox/tippecanoe).
* [Python](https://www.python.org/)
  * Geoprocessing:
    * [GeoPandas](https://geopandas.org/)
    * [Fiona](https://github.com/Toblerity/Fiona) + [Shapely](https://github.com/Toblerity/Shapely)
    * [Cartoframes](https://carto.com/developers/cartoframes/)
    * [Google Earth Engine](https://earthengine.google.com/)
  * Visualization:
    * [ggplot2](http://ggplot.yhathq.com/)
* [R](https://www.r-project.org/) - R + ggplot2 // R for stats and ggplot2 are kind of unbeatable IMHO when it comes to having a swiss army knife for data analysis and visualization. 
  * See: [Geocomputation with R](https://geocompr.robinlovelace.net/)
* [GDAL - Geospatial Data Abstraction Library](https://gdal.org/)

### Geodatabases 

* [PostGres](https://www.postgresql.org/) w/ [PostGIS](https://postgis.net/) - pretty much the standard for open source geo data management and geoprocessing. It can be pretty intimidating to set up, but you can try it out running on [Carto](https://carto.com/)
* [Mongodb](https://www.mongodb.com/) - mongodb has some spatial methods, but not as sophisticated as PostGIS!


***
***
***

## Technical References

* Technical Tools and Resources & Tutorials:
  * Map Design:
    * [Cartography Guide - Axis Maps](https://www.axismaps.com/guide/)
    * [Desktop-style cartography with web graphics - A. Woodruff](https://www.axismaps.com/nacis2019/)
    * [Watercolor Canvas Cartography](https://www.axismaps.com/blog/2019/05/watercolor-canvas/), [Watercolor Map Code](https://observablehq.com/@awoodruff/watercolor-map)
  * Web Mapping
    * [Leaflet.js](https://leafletjs.com/)
      * [GeoSandbox - Leaflet.js](https://joeyklee.github.io/geosandbox/hello-leaflet.html)
      * [Coding Train - Mapping Geolocation with Leaflet.js](https://www.youtube.com/watch?v=nZaZ2dB6pow)
    * [Turf.js](https://turfjs.org/)
      * [GeoSandbox - Turf.js](https://joeyklee.github.io/geosandbox/hello-turf.html)
      * [Mapbox - Analyze data with Turf.js and Mapbox GL JS](https://docs.mapbox.com/help/tutorials/analysis-with-turf/)
      * [Introduction to Turf.js (2015), J. Seppi](http://jseppi.github.io/intro-to-turf/#)
      * [Analyzing 60 years of tornadoes with Turf, M. Herlocker](https://blog.mapbox.com/analyzing-60-years-of-tornadoes-with-turf-857e56fa4e9f)
    * [MapboxGL.js](https://docs.mapbox.com/mapbox-gl-js/overview/)
      * [GeoSandbox - MapboxGL](https://joeyklee.github.io/geosandbox/hello-mapboxgl.html)
      * [Mapbox - Tutorials](https://docs.mapbox.com/help/tutorials/)
    * [Mapbox Studio](https://www.mapbox.com/mapbox-studio/)
      * [Mapbox - Tutorials](https://docs.mapbox.com/help/tutorials/)
    * [Kepler.gl](https://kepler.gl/)
      * [Kepler.gl user guide](https://github.com/keplergl/kepler.gl/blob/master/docs/user-guides/j-get-started.md)
      * [Animating 40 years of Earthquake data](https://medium.com/vis-gl/animating-40-years-of-california-earthquakes-e4ffcdd4a289)
    * [DataWrapper](https://www.datawrapper.de/)
      * [DataWrapper Academy](https://academy.datawrapper.de/)
    * [Carto](https://carto.com/) // // powerful for bigger datasets that you want a server to handle your geo operations on with also fast rendering. 
      * [Carto Help](https://carto.com/help/)
    * [D3](https://d3js.org/) - **advanced**
      * [Mapping With D3.js](https://mappingwithd3.com/getting-started/)
    * [Tangram](https://github.com/tangrams/tangram)
    * [Mapshaper](https://mapshaper.org/) // handy tool for exploring geodata and working on geospatial operations like simplification and other geospatial manipulation.
  * Desktop GIS
    * [GDAL - Geospatial Data Abstraction Library]()
    * [QGIS](https://www.qgis.org/en/site/)
    * [R](https://www.r-project.org/)
      * [Geospatial analysis in R](http://data-analytics.net/cep/Schedule_files/geospatial.html)
    * [Cartoframes - Python x Carto](https://carto.com/cartoframes/)
  * Color:
    * [ColorBrewer 2](http://colorbrewer2.org/#type=sequential&scheme=BuGn&n=3)
  * Other:
    * [MapShaper](https://mapshaper.org/)
    * [Awesome List: GIS](https://github.com/sshuair/awesome-gis)
    * [Deck.GL](https://github.com/uber/deck.gl)
      * [Vis Academy](http://vis.academy/#/)
    * [Google Earth Engine](https://earthengine.google.com/)


## References

* Eric Theise [Let's talk about your geostack](https://erictheise.com/geostack-deck/#/) // note licensing of the talk materials





