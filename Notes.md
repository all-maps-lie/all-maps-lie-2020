
# Materials
**NOTE: the materials are subject to change**

## Week 1: Everything is Spatial 
> "instead of focusing on how we can map the subject...[we could] focus on the ways in which mapping and the cartographic gaze have coded subjects and produced identities" - Pickles, 2004

### Lecture
* Course overview & logistics
* Introduction to critical cartography, critique, and the politics of maps

### Studio: Map Critique

### Assignment: Critical Story Map

**Brief**:

* **Map**: 
  + Using the Knight Lab's [StoryMaps] create a map that fulfills the following criteria:
    + A map with accompanying media that highlights an untold or underrepresented history or current reflection of feminism, post colonialism, and/or social or environmental justice. 
    + Your story map must be coherent and use geography as central to the telling of the story. 
    + If time is important for your story, the order of your "slides" should be ordered appropriately to best highlight the topic of choice (chronological) -- use your discretion. 
    + Possible prompts: US border issues, Global Climate protest/Fridays for Future, Global Protests, Greta Thunberg's Journey, Melting Sea Ice, Brexit, East/West Germany before end of the GDR, The Green New Deal, Policing issues, Women in science, etc.
+ **Reflect**: 
  + Document your process of using StoryMaps.
  + Reflect on what it means to research and put these points on the map. 
  + Guiding questions:
    + Who are the potential beneficiaries of your map and your story map?
    + Are your locations estimations or exact coordinates?
    + Are there potential issues for mapping these issues? Does your map endanger the people or environments in any way? Could your map lead to any false conclusions that might endanger those people or places directly or indirectly?

Be prepared to discuss your experience next week.

**Examples**  
+ A [Simple Example](https://uploads.knightlab.com/storymapjs/87f79e981dce082a57dfe2c482f65ad6/all-maps-lie-2020/index.html) for reference.
+ The MinnPost [Hockey, hip-hop, and other Green Line highlights](https://www.minnpost.com/stroll/2014/06/hockey-hip-hop-and-other-green-line-highlights/).

Alternatively: https://docs.mapbox.com/mapbox-gl-js/example/scroll-fly-to/

***
## Week 2: (Web) Cartographics
> "Cartography is not what cartographers tell us it is." - Brian Harley 

### Lecture
* Elements of (web) maps
* How to lie with maps

### Studio: Introduction to the geospatial web

### Assignment: An "Honest" Map
* Make an "honest" map. Your honest map should consider all of these components:
  * scale & "zoom"
  * projection
  * geometry
  * color
  * legend
  * clearly stated intentions, assumptions, data sources, date of production, ... 
* see: https://gisgeography.com/map-elements-how-to-guide-map-making/


***
## Week 3: Geospatial (Non)Sense
> "...Close things are more related than far things..." - Tobler's first law of geography

### Lecture
* Introduction to spatial analysis  

### Studio: Geospatial analysis on the web
* Workshop on Turf.js and Mapbox API.

### Assignment: Calculating space
* Part 1: Going the distance
  - calculate the Manhattan distance and “as the crow flies” distance between 2 points. 
  - To get Manhattan distance you must use a routing engine to calculate the distance. You can also roll your own custom solution. 
  - Report your distances in both kilometres and miles (or smaller units if appropriate) 
  - Use the mapbox placenames API to query the distance between two places using place names. 
  - Bonus:
    - Make an interface that displays those 2 types of distances given an origin and destination and show them on a map. 
    - display an aspatial representation of those distances.
* Part 2: Binning 
  *  Given [a dataset of set of points](), use a grid to calculate the following statistics for the property -- `____________` -- of the points:
     - min
     - median
     - mean
     - max
     - standard deviation 
  * Use a grid size of `50m`, `100m`, and `200m` to see how the resolution of your grid affects your interpretation.
  * NOTE: imagine using census boundaries or neighborhood boundaries - how might this affect both the visual perception of what you're representing and how you might consider normalizing your data?
* Part 3: Affective area
  - Perform a `buffer` analysis to calculate how many points in this [dataset]() would be affected by phenomenon X within `50m`, `100m`, and `200m` of this [line](). 

***
## Week 4: Locative Media

### Lecture
* Discussion on spatial data, data collection, surveillance, sousveillance, and cartographic anxiety.

### Studio: Collecting spatial data
* Workshop on 3 methods of spatial data collection using:
  * Field Papers
  * TBD
  * TBD

### Assignment
* Data collection assignment

***
## Week 5: (Counter)Mapping 
> "Cartography as a medium through which not only to reflect existing conditions of power, but also to produce new urban relationships, became an aesthetic and geographic endeavor." - Thompson, Nato. Experimental Geography: Radical Approaches to Landscape, Cartography, and Urbanism (Kindle Locations 220-221). Melville House. Kindle Edition. 

### Lecture

### Studio: Cartographic Styling
* Exploration of the MapboxGL layers API for styling basemaps and data on the fly.

### Assignment: The Map is not the Territory
* Counter-mapping assignment.

Note: https://docs.mapbox.com/mapbox-gl-js/example/toggle-worldviews/


***
## Week 6: Experimental Geography
> "we make the world, and in turn, the world makes us" - Nato Thomson, Experimental Geography
>
> "Experimental geography means practices that take on the production of space in a self-reflexive way, practices that recognize that cultural production and the production of space cannot be separated from each another,and that cultural and intellectual production is a spatial practice." - Thompson, Nato. Experimental Geography: Radical Approaches to Landscape, Cartography, and Urbanism (Kindle Locations 546-547). Melville House. Kindle Edition. 

### Lecture
* Discussion on the history of and the increasing role of new spatial media and media art in cartography & geography.
 

### Studio

### Assignment
* Final Assignment

***
## Week 7: Final Review

### Presentations
* Students will present their final projects.

### Conclusion
* Where to go from here & call to action.


<!-- 

## Workshop

* Map critique
* hello web maps w/ geosandbox
* cartographic styling with vector tiles 
* 

## Assignments

* 01: Narrative Map
* 02: 
* 03: Spatial 



 -->


<!-- 

* https://www.theguardian.com/science/blog/2018/mar/06/counter-mapping-cartography-that-lets-the-powerless-speak


Everything is spatial
(Counter)Mapping & Cartographics

Experimental geography
Radical geography
psychogeography
http://criticalgis.blogspot.com/2014/06/thinkingmaking-geographic-representation.html

https://geography.wisc.edu/cartography/education/G370/G370SP2019.html
https://geography.wisc.edu/cartography/education/G575/G575SP2019.html

https://gisgeography.com/map-elements-how-to-guide-map-making/


assignments

+ Tell a map story
+ https://storymap.knightlab.com/#examples

+ cowpath map

Assignment 1: going the distance 
- calculate the Manhattan distance and “as the crow flies” distance between 2 points. 
- To get Manhattan distance you must use a routing engine to calculate the distance. You can also roll your own custom solution. 
- Report your distances in both kilometres and miles (or smaller units if appropriate) 
- Use the mapbox placenames API to query the distance between two places using place names. 
- Make an interface that displace those 2 types of distances given an origin and destination and show them on a map. 
- Bonus: display an aspatial representation of those distances. 

Assignment 2: seeing geography: mapping cowpaths
- go and collect the paths for your assigned cowpath


# Readings
gegraphy of hate

* Politics of Design - mapping chapter
* Mark Monmonier - How to lie with maps
* cartography guide - axis maps - https://www.axismaps.com/guide/
* Robin's resources - https://github.com/tolomaps/resources
* mapschool - https://mapschool.io/
* http://www.graphicarto.com/the-lost-art-of-critical-map-reading/
* https://native-land.ca/

Topics To cover:

Start with definitions:

+ what are maps?
  + “maps are graphic representations that facilitate a spatial understanding of things, concepts, conditions, processes, or events in the human world” (Harley and Woodward 1987: xvi)
+ what is cartography?
+ what is geography?
+ what is critical?
  + Harley = "power, ideology, and surveillance"
+ What is open source?
+ Geospatial data analysis and/vs. Geospatial visualization?
+ Acknowledging land of indigenous people
+ History of mapping, roots of cartography, military connections? The weaponization of "science" in mapping...
+ dichotomies of:
  + art/science
  + objective/subjective
  + scientific/ideological
+ maps as highly partisan interventions
+ GIS as technocratic positivism <==> also potential for social good
+ Critical mapping practices:
  + carto and art, situationaists, locative art, psychogeography
  + open source mapping
+ critique in cartograpy 
  + late 80s
+ Maps and imperialist and post-colonial project



quotes:
- "close things are more related than far things" - tobler's first law of geography

# Topics:
- Introduction
  - geospatial data
- Scale
  - map scales

## Introduction: 

Geospatial Data
- what is/are data?
- where do data come from?
- what does it mean for data to be geographic?
- where are data stored
- what are geographic data formats?
- what are geographic data types?
- how do geospatial data affect/effect your data life?
- what are ways that geospatial data and computation come together?
  - routing
  - wayfinding
  - spatial analysis, geographic distributions
  - prediction/forecasting

Geographic data dimensionality and characteristics:
- data dimensions:
  - points
  - lines
  - polygons
  - surfaces
- data types:
  - nominal: name
  - ordinal: comparable by rank, orderable
  - interval: scale has no absolute "0", but can be compared to one another. e.g. you can say 5degC is 15degC less than 20degC but you cant say  that it is 3times less
  - ratio: scale has an absolute "0", e.g. money. 
  - scalar: you create your own scale that applies specifically to that data e.g. readability on a scale of 1 to 10

Spatial Considerations: All consider location, patterns, and distributions
- density
- sinuosity
- connectivity
- pattern change
- movement
- shape
- size
- isolation
- adjacency

Examples of GIS/Geospatial data analysis and computation in the wild:
- business cases
- physical science research
- social science research
- art


## Scale

Map scales
- determines how much or how little your map can hold
- See chart of map scales of USGS 
- Scale and representation
- Generalizations:
  - scale, readability, crowding
  - data availablity
  - limitations of output devices or media, e.g. print, vs. web
  - reader characteristics
- large scale == "more details, smaller area"
- small scale == "less details, larger area covered"

Different types of maps
- reference: only offer the pattern and general locations of things
- thematic: provides as much detail about a specific subject


Map projections and datums
- converting a sphere into a flat map results in distortion!
- picking the right projection
- In general, 3 families:
  - planer, conic, cylindrical
- Preserving:
  - distance
  - area
  - direction
- Projection and reprojection: rounds off tiny numbers and makes erros in position! 
- Good projections depend on accurate datum
- Geodesy is the science of accurately measuring the spherical earth
- Datum: is a model of the earth's shape that allows geodetic sceintists and surveyors to accurately measure the Earth and place the origins and orientation of the coordinate systems
  - datums depend on ellipsoids -- which are different methods and models of the earth
- Why does all this matter? GIS software needs to know what datum you're using for each set of map data you put into your database - attaching coordinates to the wrong datum can result in location and measurement errors ==> a common task in GIS is to make sure all your geo data are in the same datum before proceeding.
- Coordinate Systems and land subdivisions
  - UTM: Universal Transverse Mercator 
    - why? 
    - 1. you can measure the stuff in positive numbers from east and north regardless of what hemispehere you're in
    - 2. you never have to use negative numbers
    - uses eastings and northings
    - accuracy up to 1-meter resolution (5 digit accuracy) 
  - In the US we have a system called PLSS - public land survey system based on the Acre 1/640 of a square mile

## Reading, analyzing, and interpreting maps

- points, lines, polygons, and volumes
- Recoginizing patterns
  - Randomness
  - Clustering
  - Uniformity
- Describing patterns
  - Describing linear features
    - dendritic
    - radial
    - centripetal
    - parallel
    - trellis
    - rectangular
    - annular
  - Analyzing and quantifying patterns
    - Nearest Neighbor Statistic - determine whether a pattern of points is regular, random, or clustered. See book for nearest neighbor algorithm$$


Maps as questions and answers
- maps as media prompt further questions





 -->