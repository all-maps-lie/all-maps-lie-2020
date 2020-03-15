# Geospatial Data Guide

## What are spatial data?

Spatial data can be considered anything that has location information associated with it. In some ways *all data are spatial* - since all things happen somewhere - however there are some data that are perhaps *more spatial* than others.

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

## Projections

* See [Projections Guide](projections-guide.md)

## Geospatial data types

### Vector

Vector data are represented in the form of: points, lines, and areas. 

* **Points**: Vector data points are simply a set of x/y coordinates (vertices).
  | type | X | Y |
  | :--- | --- | ----|
  | screen coordinates | 10 | 10 |
  | coordinates in [Degrees-Minutes-Seconds](https://gisgeography.com/decimal-degrees-dd-minutes-seconds-dms/)| 123° 6' 58.4136'' W | 49° 14' 46.6512'' N |
  | coordinates in [decimal degrees](https://en.wikipedia.org/wiki/Decimal_degrees) | 	-123.116226 | 49.246292 |
  | coordinates in [UTM coordinates](https://en.wikipedia.org/wiki/Universal_Transverse_Mercator_coordinate_system) | 5454841.98N | 491540.93E |

* **Lines & Polygons**: Vector data lines and polygons are structured as a list of x/y coordinates pairs ordered in a manner such that you can join those x/y coordinate pairs to form a line or a polygon (closed or open).
  * **line**
    | type | coordinate list |
    | :--- | --------------- |
    | screen coordinates | `[ {x: 10, y:10}, {x: 10, y:20}, {x: 20, y:20}]` |
    | coordinates decimal degrees | `[{lon:-73.988, lat: 40.699}, {lon:-73.988, lat: 40.694}, {lon:-73.987, lat: 40.694}]` |
  * **polygon**
    | type | coordinate list |
    | :--- | --------------- |
    | screen coordinates | `[ {x: 10, y:10}, {x: 10, y:20}, {x: 20, y:20}, {x: 10, y:10}]` |
    | coordinates decimal degrees | `[{lon:-73.988, lat: 40.699}, {lon:-73.988, lat: 40.694}, {lon:-73.987, lat: 40.694}, {lon:-73.988, lat: 40.699}]` |
    * notice: how these coordinates are the same as the coordinates from the *line* except that the first coordinate pairs are repeated to "close" the polygon.

### Raster

Raster data (a.k.a bitmaps, images) are essentially image data - pixels or grid cells - about some kind of geographic area - usually taken from a satellite, airplane, drone, or balloon. Raster data often represent some kind of **continuous data** - e.g. topography, elevation, air pollution - but can also represent **discrete data** - e.g. land cover or land use. 

## References

* [What is spatial data?](https://www.webopedia.com/TERM/S/spatial_data.html)
* [Spatial Database - Wikipedia](https://en.wikipedia.org/wiki/Spatial_database)
* [Geographic Information - Wikipedia](https://en.wikipedia.org/wiki/Geographic_data_and_information)
* [Raster vs. Vector Data](https://gisgeography.com/spatial-data-types-vector-raster/)