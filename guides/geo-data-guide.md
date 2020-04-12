# Geospatial Data Guide

- [Geospatial Data Guide](#geospatial-data-guide)
  - [What are spatial data?](#what-are-spatial-data)
  - [What ways things can be spatial?](#what-ways-things-can-be-spatial)
  - [Geospatial data types](#geospatial-data-types)
    - [Raster](#raster)
      - [Raster Advantages and Disadvantages](#raster-advantages-and-disadvantages)
      - [Additional References: raster](#additional-references-raster)
    - [Vector](#vector)
    - [Vector Advantages vs. Disadvantages](#vector-advantages-vs-disadvantages)
  - [(Geographic) data types](#geographic-data-types)
    - [Numeric](#numeric)
    - [Nominal](#nominal)
    - [Ordinal](#ordinal)
  - [Making Data Spatial](#making-data-spatial)
    - [Geocoding](#geocoding)
    - [Data Joins](#data-joins)
    - [Georectification](#georectification)
  - [Geo Data Processing and Analysis](#geo-data-processing-and-analysis)
    - [Intro to spatial analysis](#intro-to-spatial-analysis)
    - [Spatial Data Joins](#spatial-data-joins)
  - [References](#references)

## What are spatial data?

Spatial data can be considered anything that has location information associated with it. In some ways *all data are spatial* - since all things happen somewhere - however there are some data that are perhaps *more spatial* than others. 

For the purpose of this guide, let's define spatial data as any data that either have geographic coordinates or those that can be related to a geospatial database (e.g. addressing systems). 

## What ways things can be spatial?

* Coordinate based:
  * latitude and longitude 
  * bounding boxes
* Administrative:
  * Neighborhood, City, State/Province, Region, Country, Continent name
  * Address
  * postal code
  * census tract id,
* Other identifiers pegged to geography:
  * IP Address > can be pegged to a place
  * The ever so slight variations in voltage 

*Q: What are ways of identifying the geography of data?*

## Geospatial data types

Geographic data can be collected and stored in two high level categories: as vector data or as raster data. 

![Vector vs. Raster Data]()

### Raster

Raster data (a.k.a bitmaps, images) are essentially image data - a grid of evenly sized pixels or grid cells - about some kind of geographic area - usually taken from a satellite, airplane, drone, and even balloons. Each grid cell of a raster represents a location and some kind of attribute value.

Tom MacWright explains [Raster Data](https://mapschool.io/#data) as:
> data is like a picture that you would take with a digital camera: at the lowest level of abstraction, it is a list of pixels with values. When you ‘zoom in’ and look closer at raster data, at some point you’ll see these discrete pixels, and it will look pixelated.
> 
> Raster data is used in pictures of the Earth, like those taken by satellites - but that is just the beginning. Pixels don’t need to have colors - instead, each pixel can have a number that represents height and the raster data as a whole stores elevation data. Or pixels can store temperature or reflection data and be useful for environmental work.
> ...
> Internally, raster data formats manage two tasks - packing data into pixels, and then storing the relationship between those pixels and actual places on the globe - the ‘extent’ of the data.

Raster Data formats include: GeoTIFF and JPEG2000 

So if a pixel represents geography, then this means that a pixel represents a raster data's **spatial resolution**. What determines spatial resolution for raster data? A number of factors can determine size of a raster's pixels. For aerial imagery and other earth observation applications, the resolution of a raster's pixels (aka cells) is based on the sensor that is doing the imaging and/or remote sensing. You can see that, for example the Landsat 8 Satellite has a resolution of 30mx30m while the MODIS satellite has a min resolution of 250mx250m. These resolutions were thoughtfully and carefully designed and determined based on the needs of each of these satellites' missions.

![Image of Landsat 8 Image and Modis Image]()

For the case of raster data that outputs of geostatistical models--e.g. Digital Elevation Models (DEM) or thematic landcover classification maps--then a raster's pixel size may be determined by any number of considerations including data processing power (e.g. high resolution rasters are more computationally expensive), the size of the features that are being resolved (general rule of thumb is that your feature must be at least twice as big as your pixel resolution), or to match the spatial resolution of more coarse data that is being analyzed.

Raster data often represent some kind of **continuous data** - e.g. topography, elevation, air pollution...

Imagine if this matrix represented air pollution values for a given area:
```
[
  5,  20, 51, 10,
  6,  40, 46, 20,
  10, 8,  41, 30,
  8,  2,  1,  20
]
```
where:
* 0 - 10: good
* 11 - 50: moderate
* 50>: bad


...but can also represent **discrete data** - e.g. land cover or land use. 

Imagine if this matrix represented a land cover classification of a satellite image:
```
[
  0, 1, 2, 2,
  0, 1, 1, 2,
  0, 0, 1, 1,
  0, 0, 0, 1
]
```
where:
* 0: ocean
* 1: beach/sand
* 2: grass

#### Raster Advantages and Disadvantages

| 👍 Advantages | --- |  👎 Disadvantages |
| :------------- | --- | ------------- |
| Raster is faster (computationally) than vector | --- | Raster data takes up more computer space |
| Raster data can be used to do matrix math with aerial imagery or remote sensing data | --- |  Raster data are less spatiall accurate than vector data |
| Rasters are usually the language of computer models | --- |  Less desirable visual outputs? |
| Rasters give you more surfaces to work with - more pixels == more things that can have a value | --- | ------------- |

#### Additional References: raster
* [Raster Defined - ESRI](https://support.esri.com/en/other-resources/gis-dictionary/search/raster)
* You can read more about [raster data in ESRI's guide](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/raster-and-images/what-is-raster-data.htm) and more about [raster cell size](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/raster-and-images/cell-size-of-raster-data.htm).

Read more about the [advantages and disadvantages of raster and vector data](http://planet.botany.uwc.ac.za/nisl/GIS/GIS_primer/page_19.htm)

### Vector

Vector data are represented in the form of: points, lines, and areas. 

Tom MacWright explains [Vector Data](https://mapschool.io/#data) as:
> Vector data stores basic geometries rather than pixel data. No matter how much you ‘zoom in’ on vector data, you won’t see pixels: the data stored is composed of geometric points and lines, and only converted into an image when necessary.
> 
> Vector data is used to store roads, buildings, points of interest, and other things that have some place in the world.
> ...
> Pixels in raster data will usually have attributes like color, opacity, or height. Vector data can contain much more: shapes often have rich data associated with them, usually called properties or attributes. This information can include additional numbers that describe the feature, like the number of people who live in that province, text data like the name of the town represented by a polygon, or other values like true and false.
> ...
> In addition to storing places and shapes, some vector data keeps track of topology, the relationships between different shapes. For instance, political borders often touch - you can stand with one foot in Arizona and another in New Mexico. A lot of geospatial data, though, will have one shape that represents Arizona and another that represents New Mexico, with two borders that precisely overlap, but have no other association.

Vector data formats include: Shapefiles, GeoJSON, TopoJSON, and KML.

Vector data come in 3 main flavors: points, lines, and polygons
* **points**: Vector data points are simply a set of x/y coordinates (vertices).
  * represent a discrete location. 
  * e.g. street tree locations, locations of parking ticket penalties in a city, locations of CCTV cameras
  | type | X | Y |
  | :--- | --- | ----|
  | screen coordinates | 10 | 10 |
  | coordinates in [Degrees-Minutes-Seconds](https://gisgeography.com/decimal-degrees-dd-minutes-seconds-dms/)| 123° 6' 58.4136'' W | 49° 14' 46.6512'' N |
  | coordinates in [decimal degrees](https://en.wikipedia.org/wiki/Decimal_degrees) | 	-123.116226 | 49.246292 |
  | coordinates in [UTM coordinates](https://en.wikipedia.org/wiki/Universal_Transverse_Mercator_coordinate_system) | 5454841.98N | 491540.93E |

* **lines**:  Vector data lines and polygons are structured as a list of x/y coordinates pairs ordered in a manner such that you can join those x/y coordinate pairs to form a line or a polygon (closed or open).
  * represent a linear feature
  * e.g. roads, streams, wildebeast migration routes
  | type | coordinate list |
  | :--- | --------------- |
  | screen coordinates | `[ {x: 10, y:10}, {x: 10, y:20}, {x: 20, y:20}]` |
  | coordinates decimal degrees | `[{lon:-73.988, lat: 40.699}, {lon:-73.988, lat: 40.694}, {lon:-73.987, lat: 40.694}]` |
* **polygons**: Vector data lines and polygons are structured as a list of x/y coordinates pairs ordered in a manner such that you can join those x/y coordinate pairs to form a line or a polygon (closed or open).
  * represent an areal feature
  * e.g. buildings, native land territories, areas of known whale breaching 
  | type | coordinate list |
  | :--- | --------------- |
  | screen coordinates | `[ {x: 10, y:10}, {x: 10, y:20}, {x: 20, y:20}, {x: 10, y:10}]` |
  | coordinates decimal degrees | `[{lon:-73.988, lat: 40.699}, {lon:-73.988, lat: 40.694}, {lon:-73.987, lat: 40.694}, {lon:-73.988, lat: 40.699}]` |
  * notice: how these coordinates are the same as the coordinates from the *line* except that the first coordinate pairs are repeated to "close" the polygon.

### Vector Advantages vs. Disadvantages

| 👍 Advantages | --- |  👎 Disadvantages |
| :------------- | --- | ------------- |
| Vector formats can be less bloated than raster data (but not always) | --- | Vector data need to be converted to a raster format to interface with remote sensing data or modelled data outputs |
| Vector data can be more spatially precise | --- | Doing geospatial operations with vector data is computationally expensive |
| Vector data can be prettier - nice curves! | --- | ------------- |

Read more about the [advantages and disadvantages of raster and vector data](http://planet.botany.uwc.ac.za/nisl/GIS/GIS_primer/page_19.htm)

## (Geographic) data types

Data can be broadly classified into 3 groups: Numeric, Nominal, and Ordinal Data. 

Details are from [Axis Cartography Guide - Levels of measurement](https://www.axismaps.com/guide/data/level-of-measurement/).

Knowing what your data is classified as is important for **understanding how you can represent these data and what visualization types are most effective/relevant for the data you are attempting to show**.

These data types apply generally to both raster and vector data HOWEVER, if you try to give raster data "nominal" data, you have to represent those unorderable categories numerically (e.g. 0 == "urban", 1 == "forest or vegetation", 2 == "ocean").

### Numeric

Numeric Data - anything that can be counted or measured.

* Example: “Population per square mile”
* Numeric ==> It can be counted

### Nominal

Nominal Data -  are categories that are inherently unorderable, such as dominant religion, soil types, or land-use categories

* Example: “Ethnicity”
  * Nominal - it is data that speaks to something that has been classified or otherwise given a nam 
  * It is *unorderable* ==> you can't order ethnicity in any meaningful way. Ethnicities are just names. 


### Ordinal

Ordinal Data - inherently orderable categorical data like shirt sizes (s / m / l / xl), flood risk (low risk / medium risk / high risk) or age (young / middle aged / old)

* Example: “Flood Risk”
  * Categorical data -- low, medium, high
  * They are not numeric but can be ordered in a meaningful way. 


## Making Data Spatial

Spatializing data is a super exciting and key part of working with geospatial data. There are a number of methods of taking data that do not have geographic coordinates associated with them and making those data mappable. Some of those methods are discussed in the guides linked below.

### Geocoding

Please see: [Geocoding Guide](guides/geocoding-guide.md)

### Data Joins

* See: [Attribute Join Guide](guides/attribute-join-guide.md)

### Georectification

* See: [Georectification Guide](guides/georectification-guide.md)

## Geo Data Processing and Analysis

One of the most exciting parts of working with geographic data is the ability and attempt to understand spatial relationships and patterns. There are many many approaches and 

### Intro to spatial analysis 

TBD

### Spatial Data Joins

* [Spatial Joins](guides/turfjs-spatial-joins-guide.md)



## References

* [What is spatial data?](https://www.webopedia.com/TERM/S/spatial_data.html)
* [Spatial Database - Wikipedia](https://en.wikipedia.org/wiki/Spatial_database)
* [Geographic Information - Wikipedia](https://en.wikipedia.org/wiki/Geographic_data_and_information)
* [Raster vs. Vector Data](https://gisgeography.com/spatial-data-types-vector-raster/)
* [Types of geospatial data](https://gisgeography.com/what-is-geodata-geospatial-data/)