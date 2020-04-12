# Spatial Joins with Turf.js

This is a guide to performing spatial joins in JavaScript with turf.js

## What is a spatial join?

A [spatial join](https://gisgeography.com/spatial-join/) is a special type of [attribute join](https://desktop.arcgis.com/en/arcmap/latest/manage-data/tables/joining-attributes-in-one-table-to-another.htm) that uses the spatial relationships of two datasets to calculate if/how data can be linked, merged, or *joined* from one dataset to another.

## Why spatial joins?

Let's say you wake up one day and you have an intense hankering to make a map of all the rat sightings in NYC. You do some digging around NYC's Open Data Portal and you come across two datasets: 1) [All the coordinates of rat sightings in NYC](https://data.cityofnewyork.us/Social-Services/Rat-Sightings/3q43-55fe) and 2) [Polygon data for the neighborhoods in NYC](https://data.cityofnewyork.us/City-Government/Neighborhood-Tabulation-Areas-NTA-/cpf4-rkhq). Perfect! You can make a map of the neighborhoods with the most Rats in NYC. Let's also say that these two datasets do not share any common attribute relationship like a zip code or neighborhood name. How could you create a map of NYC Rats? We could use what is called **a spatial join**!

## How do spatial joins work?

As mentioned above, a spatial join uses spatial and geometric relationships between spatial datasets to join data from one dataset to another. There are many different types of spatial joins that can occur depending on the geometry types of the datasets in question, but generally, spatial joins operate by calculating a **boolean** -- true or false -- relationship such as if features have geometries that:
* contain each other
* cross each other
* are completely within each other
* intersect each other
* ...and much more!

Depending on the **spatial join condition** that you're using to make your join, different math -- basically trigonometry -- needs to occur. You could calculate these kinds of trigonometric relationships yourself like [Dan Shiffman does in this Coding train episode of checking object intersections](https://www.youtube.com/watch?v=uAfw-ko3kB8), but lucky for us, there are tools that wrap all this math up into trusty and handy little functions. One of these such tools is a JavaScript library called [turf.js](http://turfjs.org/) -- a library for doing advanced geospatial analysis for browsers and Node.js. We will use Turf.js to cover some common examples of handling spatial joins.

# Demo: Reported NYC Rat Sightings by Neighborhood Spring (March - May) 2019 

This is a demo showing how you might use turf.js to perform spatial joins. 

## Data

1. [NYC Rat Sightings Spring, 2019](https://cdn.glitch.com/f5a2b4da-5cc8-4470-8491-987d3d2df694%2Frat-sightings-2019--spring.geojson?v=1586727112264)
2. [NYC Neighborhood Boundaries](https://cdn.glitch.com/f5a2b4da-5cc8-4470-8491-987d3d2df694%2Fnyc-neighborhoods.geojson?v=1586725147499)

## Spatial Join with `turf.collect()`: 

This makes sense when you have multiple intersecting points within a polygon. With `turf.collect()` what we are going to do is first make sure of a couple things:
1. our points are a **geojson** of a type `FeatureCollection` - a collection of points.
2. our polygons are a **geojson** of a type `FeatureCollection` - a collection of polygons.

Good, so we have the right data formats and types and now we can look at what `turf.collect()` expects as arguments. This is what the documentation shows:

```js
turf.collect(FeatureCollection<Polygon>, FeatureCollection<Point>, inProperty<string>, outProperty<string>);
```

We can see see the first two arguments are:
1. **`FeatureCollection<Polygon>`**: Our FeatureCollection of polygons -- our neighborhoods
2. **`FeatureCollection<Point>`**: Our FeatureCollection of points -- our rats
3. **`inProperty<string>`**: This is the name of the attribute in your **`FeatureCollection<Point>`** -- in the rats data -- whose values that you want to be joined to the **`FeatureCollection<Polygon>`** -- the neighborhoods. So let's say you have 5 reported rats in Williamsburg. And you set the **`inProperty<string>`** to "Status", then what you would join to **`FeatureCollection<Polygon>`** would be 5 instances of the values contained in the "Status" of the **`FeatureCollection<Point>`** in an array.
4. **`outProperty<string>`**: THis is the name of the attribute in your **`FeatureCollection<Polygon>`** -- the neighborhoods -- that will be given to the array that contains all of the collected point attributes specified in the **`inProperty<string>`**

So if we were to run the following command on our data...

```js
const neighborhoodRats = turf.collect(neighborhoods, rats, "Status", "rats");
```

...and took a look at the geojson feature for Williamsburg, our newly created data might look like this:

```js
{  type:"Feature",
   properties:{ 
      boro_code: "3",
      boro_name: "Brooklyn",
      county_fips: "047",
      ntacode: "BK72",
      ntaname: "Williamsburg",
      rats: [
        "Closed",
        "Closed"
        "Closed"
        "Closed"
        "Closed"
      ],
      shape_area: "11589988.1365",
      shape_leng: "16874.433846"
   },
   geometry{
     type:"MultiPolygon",
     coordinates:[]
   }
}
```
Notice how the `rats` property is an array of "Closed" - these are rat cases that were closed. Those are all the joins! You can imagine if the values that were joined were numeric, that you could do some summary statistics like `Math.min()` or `Math.max()` or calculate the sum, average, median, etc. In this demo, what we could do is just count how many rats per neighborhood were reported. 

And voila! You've just joined your data! 

Working Demos:
→ See the full Demo in Action: [Demo on Glitch](https://glitch.com/edit/#!/spatial-joins-nyc-rats)

### Caveats
* Spatial joins are super memory intensive. Anything larger than a couple megabytes of data and you're setting yourself up to freeze your web browser. Performing these operations work best *server-side* as a Node.js script. It is therefore recommended to do these kinds of data processing steps BEFORE you put them in the browser. Alternatively, you could try running your data processing step once in the browser (memory allowing) and then save your data out to a file which you can use in the future.

### Additional References
* → Additional demos on [Geosandbox - Oakland Crime Data Exploration](https://joeyklee.github.io/geosandbox/oakland-crime.html)
* [Turf.js - Collect](http://turfjs.org/docs/#collect)


# Additional Spatial Join Operations

Once you understand how the `turf.collect()` function works, you can start exploring some of the other spatial join methodologies. There are many other ways to perform spatial joins and turf.js provides a number of functions that allow you to check the geometric/spatial relationships between data. I've selected out a couple other turf.js functions that 

### `turf.tag()`: Join `Point` attribute to `Polygon`
> Takes a set of points and a set of polygons and performs a spatial join.

This makes sense when you know that you only have 1 intersecting point per polygon. This is known as a one-to-one spatial join.

* http://turfjs.org/docs/#tag

### Turf BooleanX functions

Turf.js comes with a BUNCH of spatial/geometry boolean functions. I suggest taking a look at some of those to learn about the possibilities. To use these, you can imagine stringing together a workflow of something like:
1. Check if dataset A intersects/overlaps/is completely within dataset B, if so then
2. merge properties from dataset A to datasetB 

These boolean functions give you a lot of flexibiity on how you want to handle joining data (either one-to-one or one-to-many) so you'll have to sort that out on your own! 

* See [Turf.js - Booleans](http://turfjs.org/docs/#booleanContains)

<!-- ### Nearest Point
> Takes a reference point and a FeatureCollection of Features with Point geometries and returns the point from the FeatureCollection closest to the reference. This calculation is geodesic.

This is handy if you're trying to do an spatial join onto a point based on the closest point feature

* http://turfjs.org/docs/#nearestPoint -->

## Next steps

Spatial joins are an essential part of the geoanalyst/cartographic toolbox. The more you work with geospatial data, you'll find that most of your job will be wrangling your data onto a common geographic shape -- usually polygons like a grid or administrative boundaries. 

With the ability to perform spatial joins, you can may have more opportunities to explore how different data or phenomenon are spatially related. You may start to flex your analytical and quantitative geographic skills -- what are the relationships that seem to emerge that you can recognize visually? what are the relationships that you can begin to quantify with statistics? Can you begin to build models? -- as well as look into other [geoprocessing](https://gisgeography.com/geoprocessing-tools/) methods that are common for achieving your mapping dreams.



