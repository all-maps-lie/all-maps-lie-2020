# Week 2: What makes a map?

> “Cartography is not what cartographers tell us it is” ― Brian Harley, 
>
> “Maps are creative statements about the world, not merely degraded reflections of it” ― Liben & Downs (1989)
>
>“Maps are graphic representations that facilitate spatial understanding of things, concepts, conditions, processes or events in the human world (Harley & woodward 1987)” - via Crampton (2010) 


## ABOUT

This week we are going to focus on answering two main questions:
1. What does it mean for something to have a location?
2. How do we translate location onto maps?

### What does it mean for something to have a location?

To examine these questions, we start by going back into history. Malcolm Lewis argues in "The Origins of Cartography" that maps are deeply situated in human evolution;spatialization being deeply intertwined with human consciousness, thought, and language. From this point of view, we might say that our desire to "place ourselves" has been part of human survival and a point of fascination since our beginnings. 

But what does it mean to "place ourselves?" From a spatial perspective, what we are referring to is *where something is located*. Have you ever thought to ask, "what is location?" What does it mean for something to have a location? Furthermore, how to do take something that has location and show where that something is? 

For thousands of years, people have have been trying to answer these questions. By reading into history we can see the myriad ways that philosophy, astronomy, and math have come to shape our understanding of geography. From the ancient number systems of the Babylonians shaping how we count to the celestial maps identifying stars like Polaris (the north star), the summation of human knowledge have been contributing directly (and indirectly) to the ways that we have come to understand *where we are in the world*. 

Some of the first "maps of the world" can be traced back to the ~500BC to the Babylonians and the early Greeks such as Anaximander and Hecataeus, but we will begin our story this week with a particularly influential character named Eratosthenes. Eratosthenes was a Greek scholar in ~200BC whose works are reflected in how we've come to understand and represent location. He is perhaps one of the first to propose the first calculation of the earth's circumference, to calculate the tilt of the earth's axis, and is credited with incorporating the use of parallels (horizontal) and meridians (vertical) lines to divide a map such that the relative distances between places could now be more easily linked (this is a massive thing!). Eratosthenes's Geography was more than just clever experiments to prove his assertions about earth's spherical shape and it's size, but also reflected an understanding of where things might be located as a function of the reported daylight hours of a place. This would come to inform what we now call, latitude--the north/south location on earth. Eratosthenes's work was further developed by another fellow Greek by the name of Hipparchus (~BC120) who sought to create more accurate ways of deriving latitude and established early ideas around the relationship between time and place for deriving a location from east to west. This was the beginnings of an understanding of *longitude*. 

Central to the development of understandings of "where" things were in the world came from examining the works and records of the civilizations and empires of the past. Fast forward ~100 years and the Roman Empire had expanded across much of what is now known today as Europe and North Africa. The Romans kept extensive records of "where" things were, the "Milliarium Aureum" being a symbol and marking point from which all distances were measured. The saying "all roads lead to Rome" is associated with this marker. What is significant about the Milliarium Aureum is that it marked a stable location relative to which distances could be measured and, with such an extensive empire, a phenomenal "dataset" from which maps of the world could be made. Enter Ptolemy. 

Ptolemy, a Greek Scholar living in Alexandria ~150AD, was a rather keen data collector. In his *Geography* he created an extensive Gazette of the locations of the Roman Empire along with other known locations. Using this he created instructions of how to create maps of the world, using latitude (*climata*, as a function of daylight hours) and longitude (as a function of time, based at what he defined as 0 degrees located over Fortunate Isles rather than those that had been done previously by geographers like Eratosthenes and Hipparchus, which were centered roughly around Alexandria) in coordinate degrees. Despite the blank spots on the map, we can see the beginnings of the cartographic systems and conventions being made! Ptolemy is also known to be one of the first to record observations of the Polaris (the North Star) which is important for our understanding of latitude.

However erroneous these maps may have been, the contributions of these early scholars to positional awareness were central to the establishment of mapping, cartography, and exploration. Fast forward over a thousand years, particularly to the Age of Discovery (starting ~1400s). Maritime exploration, colonization, and global trade was happening like never before. New map projections like Gerardus Mercator's, Mercator projection, allowed for less precarious nautical travel -- by preserving angular direction, as long as sailors could keep at a constant direction, they would make it to their destination -- and new sailing technology made long maritime travel faster. Increasingly more places were being "put on the map" and with inventions like the marine chronometer (late 1700s) invented by John Harrison, travelers could now accurately determine longitude at any time and place also allowing people to correct inaccuracies in previously mapped locations.

By the 1800s -- long before satellite GPS -- there were now ways to accurately locate places on earth. The prime meridian had been set by the British at Greenwich, UK which set the (arbitrary) global standard for 0° longitude and  0° latitude was defined (less arbitrarily you can say) at the equator. With a set 0°,0° and with accurate chronometers that could keep accurate time with Greenwich, UK, the world now could express location--where something is--better than ever before. By extension things could be mapped better than ever. What did it look like to put a place on a map? The answer to this is simply: with a lot of work... and surveying!

Cartographic data collection is knowing about where things are. As we saw with how we measure longitude, knowing *where something is* means knowing *where something is relative to something else*, usually a fixed location and time. By looking at the early surveying tools such as the [Gunter Chain]() and [surveyor's compass](), you can see that with relatively simple tools, you can produce detailed spatial data and as a result, detailed maps; maps of the [Great Lakes]() and the [Great Trigonometrical Survey of India]() are great examples of these tools and methods in action. Now with locational technologies such as [satellite GPS](https://www.youtube.com/watch?v=FU_pY2sTwTA) in conjunction with tools like [wifi sensing](https://slate.com/technology/2018/06/how-google-uses-wi-fi-networks-to-figure-out-your-exact-location.html) and [bluetooth locations tracking](https://electronics.howstuffworks.com/bluetooth-surveillance2.htm) there are many ways to locate things in the world. However, much of the geographic data we collect isn't just about location anymore. The most interesting things arise when we start to look at geographic data that have more to say about where things are, but rather what is happening and where they are happening. 

The next section takes a closer look at what it means to use location data to produce maps and review some fundamental concepts to understand what makes a map. 

### How do we translate location onto maps?

In the previous section, I gave a (rough) overview of what it has meant to locate things. As a quick review:
1. throughout history, people have long tried to understand where things are in the world,
2. we tell where something is by coordinates expressed as latitude (where we are north or south of the equator) and longitude (where were are east or west of the prime meridian),
3. the tools to locate things are relatively simple, and
4. lastly, knowing where things are is helpful for navigation and for reference, but there's a lot more we can learn from geographic data.

<!-- We learned about how location was determined and derived over the centuries -- with math -- and how location is derived now -- with satellite GPS. To say the least, it is all very impressive.  
-->

So, I think it is safe to say the earth is round. Actually, it is more safe to say that the earth is round-ish. Let's take that even further. The most correct thing we can say is that the earth is a blobby, round **geoid**. According to wikipedia, "The geoid is the shape that the ocean surface would take under the influence of the gravity and rotation of Earth alone, if other influences such as winds and tides were absent. This surface is extended through the continents." [Geoid](https://en.wikipedia.org/wiki/Geoid). The earth is actually really funky looking and it turns out that this is actually really important for our understanding of where things are located and where things eventually get rendered on a a map. Here's why:

1. **Regarding positional accuracy**: all of the fancy math that those old Greeks worked out back then didn't factor in the earth's blobbiness. If we really want to get super accurate with location, then we need to have an accurate model of the earth's blobbiness -- the geoid. Because geoids are super complex to determine location, what we end up using is what is known as a reference ellipsoid (aka reference spheroid or datum). 
3. **Regarding translating a 3D world into 2D**: Taking a 3D blobby thing and flattening it onto a 2D plane is actually really hard. What map makers like Gerardus Mercator worked out was what is called **projection** or a mathematical way to translate a 3D world (not a geoid, but a spherical ellipsoid) onto a 2D plane by introducing distortions to either angular direction, area, and/or location. Have you ever tried to peel an orange in one piece? Projections offer a way to flatten a 3D thing so it can be represented in 2D. 

#### Geographic coordinate systems 

The first point to understand when putting something on a map is to account for the reference ellipsoid (aka reference spheroid or datum) on which the locational data was based on. As noted in this reference post, ["The geoid, ellipsoid, spheroid, and datum, and how they are related"](https://desktop.arcgis.com/en/arcmap/10.3/guide-books/map-projections/about-the-geoid-ellipsoid-spheroid-and-datum-and-h.htm), you can see how positional accuracy can vary depending on which reference ellipsoid was used. Different GCS exist as a way of prioritizing locational accuracy depending on the context that your geographic data will be relevant. For example if you're striving for the most positional accuracy and you're in North America, you might use the NAD83 GCS over the WGS84 GCS which is more globally accurate. Similarly if you are in Australia, you might use GDA94 which is more accurate for Australia over the WGS84.

It is super important to keep track of what reference ellipsoid your various data collection devices (e.g. GPS) and data sources are based on when making projects with geographic data. As you can see in the screenshot below, these positional inaccuracies can lead to false conclusions about where things are located. 

![Differences in locations based on NAD27 and NAD83](../assets/images/gcs--differences.png)

Luckily for us, modern technology coupled with some really smart and clever contributions from geographers (in their many shapes and forms) make it relatively simple to translate between reference systems in case you realize that your data are based on different coordinate reference systems.

#### Projections

So you've you've made sure all your data are aligned correctly based on the GCSs of your data, how do you get this 3D world onto a 2D map? Well, it's time to choose a projection. Before we choose a projection though, let's take a second to understand what a projection is and how it works.

As I mentioned earlier, in order to make a map -- that is, translating a 3D sphere onto a 2D plane -- you have to do project your data. A projection is "a complex mathematical method of representing our three dimensional earth in a flat, two dimensional context". Projections preserve EITHER direction (angles), size (area), or distance. There are 3 types of projections named based on what aspect they preserve:
1. **conformal**: preserves angles - the relative angles at all points of the map are correct
  + e.g. mercator projection, 1569
2. **equal area**: preserves area by compromising scale, angles, and shape
  + e.g. Mollweide projection, 1805
3. **equidistant**: preserves the distance between 2 specific points on the map
  + e.g. Azimuthal projection, ~11th century

There are a number of map projections. Dozens actually! You can see them all in action here [D3 Map projection showcase](https://bl.ocks.org/mbostock/29cddc0006f8b98eff12e60dd08f59a7). 

Some map projections like the [Robinson projection](https://en.wikipedia.org/wiki/Robinson_projection) attempt to "compromise" on all those aspects of area and angles. Depending on your take on things, this is either a good thing because it spreads the error "equally" as much as possible or a rather bad thing in that nothing about the map is right in the end. 

Map projections are incredibly important! They pretty much lie at the heart of what it means to represent geography. You can see accidental geographic misrepresentations all over the place where the uses of projections mislead map readers. Sometimes the use of inappropriate projections are not accidental but rather chosen specifically for political purposes to intentionally mislead map readers. Either way map projections are one of the most important considerations to take into account when making a map. 

Map projections are complex math that get applied onto geometry. Figuring out all this math is exciting and super cool, but it is *very* complex and not for the faint of hearted. Lucky or us many smart people exist in the world and have worked out all of these mathematical transformations for us. All we need to do is know how to use them, when to use them, and where (in which software) we can use them. This is where geographic information systems (aka GIS) come in handy!

#### Geographic information systems (GIS)

A GIS is a system of managing, analyzing, and rendering, geographic data. GISystems are more than just software--including everything including people, methods, data, and hardware--but for the purpose of this post I will focus on the software aspects.

GISs allow us to handle everything we've talked about so far from geographic coordinate systems to the many projections that allow for geographic data to be analyzed and rendered.

**GIS allows us to manage geographic data**: Managing geographic data means handling many different spatial data formats (we'll talk about this below) and allowing for coordinate system and projection conversions to be done.

**GIS allows us to do geographic analysis**: Geographic analysis is spatial--where things are--and geometric. To do spatial analysis, often times were not only looking to see where things are, but we also need to know how things are interacting. With GIS we can answer how things intersect or overlap or what occurs if spatial elements are added or subtracted and more. 

**GIS allows us to render geographic data**: Not all GIS have methods for rendering, but many/most of them do. Rendering geographic data means knowing how projection information is applied to geographic coordinates to represent those data on some kind of canvas. Usually you can export data to images or PDFs or other similar formats. 

There are many GIS softwares out there ranging from commercial, proprietary solutions like ESRI's ArcGIS to more open source solutions like QGIS or GrassGIS. These software are based on many of the same fundamental software libraries such as GDAL/OGR, PROJ, Mapnik, and GEOS which provide computational solutions to projections, rendering, and data management. 

#### Geographic Data and Geographic Data formats

Geographic data can be collected and stored in two high level categories: as vector data or as raster data. 

##### Raster

Tom MacWright explains [Raster Data](https://mapschool.io/#data) as:
> data is like a picture that you would take with a digital camera: at the lowest level of abstraction, it is a list of pixels with values. When you ‘zoom in’ and look closer at raster data, at some point you’ll see these discrete pixels, and it will look pixelated.
> 
> Raster data is used in pictures of the Earth, like those taken by satellites - but that is just the beginning. Pixels don’t need to have colors - instead, each pixel can have a number that represents height and the raster data as a whole stores elevation data. Or pixels can store temperature or reflection data and be useful for environmental work.
> ...
> Internally, raster data formats manage two tasks - packing data into pixels, and then storing the relationship between those pixels and actual places on the globe - the ‘extent’ of the data.

Raster Data formats include: GeoTIFF and JPEG2000 

##### Vector

Tom MacWright explains [Raster Data](https://mapschool.io/#data) as:
> Vector data stores basic geometries rather than pixel data. No matter how much you ‘zoom in’ on vector data, you won’t see pixels: the data stored is composed of geometric points and lines, and only converted into an image when necessary.
> 
> Vector data is used to store roads, buildings, points of interest, and other things that have some place in the world.
> ...
> Pixels in raster data will usually have attributes like color, opacity, or height. Vector data can contain much more: shapes often have rich data associated with them, usually called properties or attributes. This information can include additional numbers that describe the feature, like the number of people who live in that province, text data like the name of the town represented by a polygon, or other values like true and false.
> ...
> In addition to storing places and shapes, some vector data keeps track of topology, the relationships between different shapes. For instance, political borders often touch - you can stand with one foot in Arizona and another in New Mexico. A lot of geospatial data, though, will have one shape that represents Arizona and another that represents New Mexico, with two borders that precisely overlap, but have no other association.

Vector data formats include: Shapefiles, GeoJSON, TopoJSON, and KML.



#### Web Maps and Web Mapping




## TABLE OF CONTENTS

- [Week 2: What makes a map?](#week-2-what-makes-a-map)
  - [ABOUT](#about)
    - [What does it mean for something to have a location?](#what-does-it-mean-for-something-to-have-a-location)
    - [How do we translate location onto maps?](#how-do-we-translate-location-onto-maps)
      - [Geographic coordinate systems](#geographic-coordinate-systems)
      - [Projections](#projections)
      - [Geographic information systems (GIS)](#geographic-information-systems-gis)
      - [Geographic Data and Geographic Data formats](#geographic-data-and-geographic-data-formats)
        - [Raster](#raster)
        - [Vector](#vector)
      - [Web Maps and Web Mapping](#web-maps-and-web-mapping)
  - [TABLE OF CONTENTS](#table-of-contents)
  - [OUTCOMES & GOALS](#outcomes--goals)
  - [PACING / DURATION](#pacing--duration)
  - [TOPICS](#topics)
  - [REFERENCES](#references)
  - [STUDIO](#studio)
  - [ASSIGNMENT](#assignment)

## OUTCOMES & GOALS


## PACING / DURATION

* :05 - Project Highlight
  * :05m - Project Highlight: Ben Wellington, IQuantNY
* :15m - Review
  * :10m - Review: week 1 review & questions
  * :05m - Review: week 1 data scavenging
* :40m - Discussion
  * :25m - TBA
  * :10m - Assignment #2: web mapping exercise & Final project proposal
* :90m - Studio
  * :05m - bio-break
  * :30m - Studio: Anatomy of a web map & geographic data
    * (very) Brief history
    * Basic principles
  * :25m - Studio: Introduction to web mapping
    * Selected Web mapping platforms
    * Selected Javascript libraries
  * :20m - Studio: Independent Leaflet mapping exercise
  * :10m - Studio: Show & Tell


<!-- * :60m - lecture & discussion
* :10m - break
* :70m - intro to web mapping
* :10m - assignment overview -->

## TOPICS

This week we are going to focus on:



## REFERENCES

* See [Week 2 Readings and Project References](../BIBLIOGRAPHY.md#week-02-countermaps--cartographics).

***
***
***

## STUDIO

* ↳ [Link to Studio](#).

***
***
***

## ASSIGNMENT

* ↳ [Link to Assignment](../assignments/assignment_02.md).


<!-- 
 This week is called "Countermaps and Cartographics." "Countermaps" refer to efforts to map "against dominant power structures" and "Cartographics" are reference to the visual manifestations of various spatial mappings. These terms are relevant for us because we will be focusing on ways in which our contributions - albeit still in their early stages - can be framed as mini "resistances." 

This week will be exploring how "countermaps" and "cartographics" can take the form of "map mashups and new spatial media" and how they relate to media art/creative technology. Our discussion will address this question "what is critique?" and the role that media art/creative tech interventions may play in shaping cartographic discourse. The discussion will explore how the changing landscape of tools and participants in mapping and map making have shaped who, how, and what maps operate in the world. 

This week we will focus on web mapping "map mashups." Using the data we collected from last week, we will take a look at programmatic methods for making interactive maps using Leaflet.js. We will also take a look at Kepler.gl, a web-based GUI tool for visualizing spatial data.

* what's on a map? and what power do maps wield?
  * Countermaps & Cartographics: 
    * On geographic knowledge, geography, cartography, mapping & GIS: Overview of GIS, Geography, and Discipline of Cartography - and where we fit in
    * Countermaps:
      * What can maps do? 
      * Examples of ways in which maps make space and knowledge
    * Cartographics: "A Map is not the territory" - https://en.wikipedia.org/wiki/Map%E2%80%93territory_relation
      * Elements of a map? 
      * Mark Monmonier - How to lie with maps ==> about cartographic considerations
    * Studio:
      * getting coordinates from photo metadata and saving to a file
    * A2: Points on the map 
      * continue data collection, go through geosandbox 
      * publish your map with images that explain what you have collected so far.



**Chapter 2:**
1. What is critique? How can mapping be critical? The concept of "Situated Knowledges" and the production of space
2. Basic Principles of Critical Cartography
   1. Via Crampton
      1. Critique has a number of basic principles. First, it examines the (often unexamined) grounds of our decision-making knowledges; second it situates knowledge in specific historical periods and geographic spaces (rather than being universal for all time); third it seeks to uncover the relationship between power and knowledge; and fourth it resists, challenges, and sometimes overthrows our categories of thought. The purpose of critique is not to say that our knowledge is not true, but that the truth of knowledge is established under conditions that have a lot to do with power. Critique is therefore a politics of knowledge. Crampton, Jeremy W.. Mapping (Critical Introductions to Geography) . Wiley. Kindle Edition. 
   2. Via Blomley
      1. 1. It is oppositional: it targets dominant forms of oppression or inequalities. 2. It is activist and practical: it wishes to change the world. 3. It is theoretic: it rejects positivist explanation and embraces critical social theory. Crampton, Jeremy W.. Mapping (Critical Introductions to Geography) . Wiley. Kindle Edition. ... Critical cartography and GIS is only in part a matter of scholarship, for the other half of our one–two punch, we have to turn to actual interventions, protests, transformations, and community mappings. Included in this would also be art work, blogs, mashups, and the “geospatial” web. Crampton, Jeremy W.. Mapping (Critical Introductions to Geography) . Wiley. Kindle Edition. 
   3. In sum:
      1. 1. The first principle of critical mapping is that maps are incredibly useful ways of organizing and producing knowledge about the world, but that these orders of knowledge also incorporate unexamined assumptions which act as limits which deserve to be challenged. 2. One way to challenge these orders of knowledge is by putting them into historical perspective. This historicization of knowledge not only shows that other times did things differently, but by providing an intellectual history it allows us to see the edges of our own limits, and to conceive of other knowledges that might be useful. Critical mapping also emphasizes that the way maps and spatial knowledges have been deployed has varied tremendously between cultures and places. This can be described as a spatialization of knowledge. 3. Critical mapping also holds that geographic knowledge is shaped by a whole array of social, economic, and historical forces, so that knowledge does not exist except in relation to power. When we speak of maps as political, it is this relationship between knowledge and power that is at stake. 4. The critical mapping project is also one which has an activist, emancipatory flavor to it. Sometimes this approach is concerned with overthrowing the influence of official knowledges (such as those of the government or the state) by showing their historical and spatial contingency (Livingstone 2003; Sparke 1998). At other times this approach seeks to dismantle more specific forms of knowledge, such as recent work by feminists in critical GIS or community activism in participatory GIS (Elwood 2006b; Kwan 2002a; Schuurman 2002). Crampton, Jeremy W.. Mapping (Critical Introductions to Geography) . Wiley. Kindle Edition. 
3. Maps are active; they actively construct knowledge, they exercise power and they can be a powerful means of promoting social change. Crampton, Jeremy W.. Mapping (Critical Introductions to Geography) . Wiley. Kindle Edition. 
4. Wood argued that maps express the interests of certain groups and that these interests are not always explicit. Crampton, Jeremy W.. Mapping (Critical Introductions to Geography) . Wiley. Kindle Edition. 
5. Rejecting the binary oppositions until then dominant in cartography, such as art/science, objective/subjective, and scientific/ideological, Harley sought to situate maps as social documents that needed to be understood in their historical contexts.

Crampton, Jeremy W.. Mapping (Critical Introductions to Geography) . Wiley. Kindle Edition. 





 -->