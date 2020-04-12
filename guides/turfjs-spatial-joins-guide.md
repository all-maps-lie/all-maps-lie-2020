# Spatial Joins with Turfjs

This is a guide to performing spatial joins with turf.js

## What is a spatial join?


A [spatial join](https://gisgeography.com/spatial-join/) is a special type of [attribute join](https://desktop.arcgis.com/en/arcmap/latest/manage-data/tables/joining-attributes-in-one-table-to-another.htm) that uses the spatial relationships of two datasets to calculate if/how data can be linked, merged, or *joined* from one dataset to another.


## `turf.tag()`: Join `Point` attribute to `Polygon`

This makes sense when you know that you only have 1 intersecting point per polygon. 

* http://turfjs.org/docs/#tag

## `turf.collect()`: 

This makes sense when you have multiple intersecting points within a polygon.

* http://turfjs.org/docs/#collect

## Nearest Point

* http://turfjs.org/docs/#nearestPoint


## Nearest Point on Line

* http://turfjs.org/docs/#nearestPointOnLine

## Turf BooleanX functions

* http://turfjs.org/docs/#booleanContains 