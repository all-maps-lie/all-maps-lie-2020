# OpenStreetMap Overpass API

This is a guide about [Overpass Turbo](https://overpass-turbo.eu/) - a tool and API for querying and retrieving data from the OpenStreetMap.

## Vocabulary

The OverpassAPI is super handy, but the vocab and terminology I've always found to be a bit hard to manage. Here's some terms you might encounter. The Overpass API also has their [glossary](https://dev.overpass-api.de/overpass-doc/en/preface/glossary.html).

### Terms related to how Overpass refers to OpenStreetMap Data:
| term | definition | additional reference |
| :--- | ---------- | ---- |
| **node** | Represents data for a single coordinate | `node()` |
| **way** | Represents data for a polyline | `way()` |
| **relation** | Represents anything that is beyond the scope of a node or way. Basically it is like the polygons of OSM. | `rel()` |
| **area** | represents an OverpassAPI specific data type regarding areas of things - a work around since OSM only uses nodes, relations, and ways as their data types. | ---- |

For additional terms do check out the [Overpass Glossary](https://dev.overpass-api.de/overpass-doc/en/preface/glossary.html)

### Terms related to overpass queries

The Overpass API is extensive and sophisticated. You can do SO much with it when it comes to getting OSM data. That being said, I feel like it is the equivalent to learning a new programming language since it is so extensive and requires understanding and knowledge of how OSM structures and labels data, all the terminology is new, they have their methods of structuring queries, etc etc. Overpass is awesome, but whew, it can feel overwhelming. 

Anyhow, here's a few handy descriptions of syntax for the Overpass Query Language (Overpass QL).

| term | definition | arguments |
| :--- | ---------- | ---- |
| **nwr()** | is a function for getting nodes, ways, and relations for the given argument - usually a `{{bbox}}`or bounding box coordinates | bounding box |
| **node()** | is a function for getting nodes for the given arguments | bounding box |
| **way()** | is a function for getting ways for the given arguments | bounding box |
| **rel()** | is a function for getting relations for the given arguments | bounding box |
| **out** | this specifies that this is where you call your output based on all the queries your defined above | `geom | center ` |

* Bounding boxes are defined as so: 
  * `(minimum latitude, minimum longitude, maximum latitude, maximum longitude)`
  * e.g.: `nwr(minimum latitude, minimum longitude, maximum latitude, maximum longitude)`
  * e.g.: `nvw(50, 6, 52, 7)`
* From [Overpass_API_by_Example](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_API_by_Example): The `out` statement has various modes to address this problem in a more convenient way: You can choose for example `out geom` to let Overpass API resolve the coordinates for you. Or you use `out center` to collapse the geometry to a single coordinate per object.

<!-- Some handy statistical operators
| term | definition | additional reference |
| :--- | ---------- | ---- |
| **count()** | ---------- | ---- | -->

## Handy Snippets

In these examples we return the `geom` which is a GeoJSON object since most of the time we want to get back the data in a friendly format. 

### Retrieving all nodes, ways, and relations in a `bbox`

```
nwr({{bbox}});
out geom;
```

### Retrieving specific nodes, ways, and relations with a specific property

```
nwr[man_made="storage_tank"]({{bbox}});
out geom;
```

### Retrieving specific `node`s and their geometry:

```
node[highway=bus_stop]({{bbox}});
out geom;
```

### Retrieving specific `way`s and their geometry:

```
way[man_made="storage_tank"]({{bbox}});
out geom;
```

### Retrieving specific `rel`ations and their geometry:

```
rel[from="London Fenchurch Street"]({{bbox}});
out geom;
```

## Really Super Cool Snippets to Inspire

### Chaining Queries

This command says: 
* give me all the nodes, ways, and relations for all the public transport tagged as a `station` in the bounding box. 
* then, select all of the nodes, ways, and relations tagged as `supermarket` that are **around: 100** meters of those `stations` selected before.
* then, output the **center** of the selected `supermarket` data.
```
nwr[public_transport=station]({{bbox}});
nwr[shop=supermarket](around:100);
out center;
```

## References

* See: [Spatial Data Selection - Overpass API](https://dev.overpass-api.de/overpass-doc/en/full_data/index.html)