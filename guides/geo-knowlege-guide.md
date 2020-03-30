# Geo Knowledge Guide

A vastly reductive, but valiant attempt to catalog some of the major touch points of what I might consider "geographic knowledge" or thinking. This will give you an idea of things to aspire to given that we will barely scratch the surface of just a handful of these topics.

This guide is important because it covers some of the domains of interest that are helping to theoretically and practically frame the course.

- [Geo Knowledge Guide](#geo-knowledge-guide)
- [Geography - Human & Physical](#geography---human--physical)
  - [Human Geography](#human-geography)
  - [Physical Geography](#physical-geography)
  - [The need for both](#the-need-for-both)
  - [Why this matters](#why-this-matters)
- [Mapping: Cartography, GIS, & Remote Sensing](#mapping-cartography-gis--remote-sensing)
  - [Definitions](#definitions)
    - [Mapping](#mapping)
    - [Cartography](#cartography)
    - [Geographic Information Systems (GIS)](#geographic-information-systems-gis)
    - [Remote Sensing](#remote-sensing)
- [Mapping Roadmap](#mapping-roadmap)
  - [Domain Knowledge](#domain-knowledge)
  - [Front-end](#front-end)
    - [Cartographic Fundamentals](#cartographic-fundamentals)
      - [Symbology / Visual Variables](#symbology--visual-variables)
      - [Projections](#projections)
      - [Color & Maps](#color--maps)
      - [Scale & Generalization](#scale--generalization)
      - [Labeling and text](#labeling-and-text)
    - [Reference Map Types](#reference-map-types)
    - [Thematic Map Types](#thematic-map-types)
      - [Choropleth maps](#choropleth-maps)
      - [Proportional Symbols](#proportional-symbols)
      - [Dot Density](#dot-density)
      - [Cartograms](#cartograms)
    - [Web Mapping](#web-mapping)
      - [HTML5](#html5)
      - [Pick a web mapping application tool](#pick-a-web-mapping-application-tool)
      - [Pick a web mapping framework](#pick-a-web-mapping-framework)
    - [Desktop GIS](#desktop-gis)
  - [Back-end](#back-end)
    - [Geographic Data](#geographic-data)
    - [APIs](#apis)
      - [Static Imagery](#static-imagery)
      - [Routing](#routing)
      - [Placename Search](#placename-search)
      - [Datasets](#datasets)
  - [DevOps](#devops)
- [Everything Besides the Map](#everything-besides-the-map)
    - [Databases](#databases)
    - [Full stack web development](#full-stack-web-development)
    - [Statistics](#statistics)
    - [Data Visualization](#data-visualization)
    - [Domain Expertise](#domain-expertise)

# Geography - Human & Physical

Capital "G" Geography is more than just state capitols and maps. In fact, a lot of Geography has nothing to do with those things and is rather about problematizing or critiquing those things. 

Capital "G" Geography is about considering the geography of a place and its role in shaping and being shaped by some aspect of social or physical processes. In any given Geography department, you might have people studying any number of things including: the "Geography of Scandanavian Death Metal", the "Geography of youth radicalization in recently immigrated populations", "The effects of sediment runoff in glacial melt", and "The effects of street trees in atmospheric turbulence in suburban neighborhoods" - the breadth and depth of expertise couldn't be greater! 

The point here is that, for Geographers and the discipline of Geography, the geographic context is critical to understanding/appreciating the history, politics, culture, physical nature of a phenomenon. This may seem like a given, but other disciplines do not prioritize or sometimes even consider spatial context or localization as a relevant factor.

For the purpose of this class, I think it is helpful to introduce some of these disciplinary concepts (though the boundaries can be fuzzy) to help give you an overview of where you might situate your work. 

## Human Geography

Human geography is concerned with human processes. These processes include topics across a range of disciplines such as economics, demographics, political science, psychology, sociology, gender studies, queer studies, media studies, history, and more. Often times these disciplines get framed as `________` Geography such as Economic Geography, Political Geography, War Geography, Feminist Geography, and so on. 

Some examples of human geographers and their work:
* ...
* ...
* ...


## Physical Geography

Physical geography is concerned with biophysical processes. These processes include topics across a range of disciplines such as geomorphology, meteorology, climatology, biogeography, ecology, soil science, forestry, hydrology, atmospheric science, and more. To be a physical geographer often means you studied within a Geography department, learning to consider the deep importance of geography - social and physical contexts - in shaping society and space all the while focusing on some realm of the environmental sciences. 

Some examples of physical geographers and their work:
* ...
* ...
* ...


## The need for both

The divisions between Human and Physical Geography are definitely real. Whether disagreements occur over methodological approaches or theoretical ones, it can be pretty surprising how different these two approaches to Geography can be. However different the two types of Geography may be, I would argue for the necessity for both to live together. The beauty of having these sometimes radically different universes colliding together is that it can help us to consider as many perspectives, impacts, and realities of the same phenomenon.

For instance, let's take an Urban Geography example. Imagine that the city of New York is trying to start a program to offer carbon offsetting credits at the neighborhood scale for maintaining street trees and other urban vegetation. *Physical geographers* studying urban ecology might offer up their skills and use a combination of aerial imagery to quantify the number of trees in the city and then use physical measurements of sap flow on a sample of trees throughout the city to understand their health. This could easily be the end of the story, however, the implications of this exercise become apparent by way of Human Geography research. Taking this thought experiment further, *Human geographers* might launch a critique against this approach because such  quantification may disadvantage neighborhoods who have historically not had the capacity or funding to maintain the trees and vegetation around them. Furthermore, Human Geographers might be the first to point out how historically, racist policies have pushed black and other minority groups to environmentally unfavorable locations that might be less conducive for healthy plants. Taken together, the city might have a more holistic understanding of A) how to undertake such a study/employ such a policy and B) how to ensure that we do not reinforce legacies of racist or unfair policies that further disadvantage people and communities. The back and forth between these two modes of thinking and their approaches are what make Geographic thinking important for how we approach complexity in the world! 

Aside: I will acknowledge there are lots of people who fall in between Human and Physical geography and even more people who don't even recognize that the work they are doing might even be classified as existing in this "third space." I might be one example of this. While I am all for the radical overlaps, interdisciplinary collaborations and remixing, I think recognizing disciplinary histories and politics is super important and therefore am not sure about "antidisciplinarity" as a solution but rather just another approach (with mixed feelings 😬). 

## Why this matters

You may be thinking, so what? Why is this relevant for me in this class?

This matters because this is what we are going to practice in this class: simultaneously embracing and critiquing geography and technology. 

We are going to be using tools and methodologies that can change *how we understand* geography (think: the Physical geographers above) all the while critiquing (think: Guman geographers above):
* A) those understandings, their limits, and their implications and 
* B) the tools, the data, and knowledge that frame *how we understand* and *what we can understand* about the geographies we are exploring.

What's exciting is that at least by recognizing the existence of such disciplines, you may find literature and projects that help you to frame your work in past and present research. IMHO there's nothing more exciting that reading a book or article where every sentence seems to eloquently articulate all those thoughts in my brain! 

***
***
***

# Mapping: Cartography, GIS, & Remote Sensing

This section is dedicated to highlighting some key aspects of mapping from the disciplinary perspective and the skills involved.

## Definitions

I will preface this by saying that the boundaries aren't clear cut and defined.  

### Mapping

![Aerial Bold ABC Book](https://benedikt-gross.de/thumbs/projects/abc-the-alphabet-from-the-sky/b-2400x1230-q80.jpg)

*Mapping* is maybe the broadest and most inclusive word for describing the process of collecting "data" and representing those data relative to one another. It doesn't necessarily need to refer to geographic mapping - e.g. stakeholder mapping, projection mapping, etc - but this is mostly what we'll be talking about in this class. 

Axis Maps has an approachable and thoughtful answer to this question of "what is a map?" in their [Cartography Guide](https://www.axismaps.com/guide/general/what-is-a-map/) which says that a "a map is a representation of a place." If we apply this to the term **mapping**, we can consider that **mapping** is about the process of representing places. 

In this class, we are most concerned with **mapping** and making **maps**. To do our *mapping* we will consider cartographic methodologies and those from our own media art and creative tech backgrounds. 

### Cartography

![Census Map](https://www.axismaps.com/guide/general/what-is-a-map/thematic_map.png)
via [Axis Maps](https://www.axismaps.com/guide/general/what-is-a-map/)

Cartography may be best defined as the study and practice of making maps. Cartographers are concerned with the mapping process - from  data collection to representation. As a focal point, cartographic representation can include a number of considerations such as how geographic data and their context are visualized (symbology), generalized (scale), labeled, and projected (taking a 3D world and making it flat).

The lines may be fuzzy between where Cartography, GIS, and Remote Sensing start and end, but ultimately, if maps are involved, so it cartography.

As will be revealed to you in Jeremy Crampton's [Critical Introduction to Cartography and Mapping]() there are are LOTS of feelings and thoughts about how cartography is framed. 

### Geographic Information Systems (GIS)

![QGIS Screenshot](https://i.stack.imgur.com/SSqLZ.png)
vis [GIS Stack Exchange](https://gis.stackexchange.com/questions/210684/qgis-2-14-6-processing-extension-polygonize-tool-missing)

GIS refers both to a discipline and the tools. **As a tool**, a GIS is basically a system - software, tools, and methods - of collecting and managing geographic information. Like any other software, a GIS might take the form of a database with additional capabilities of handling spatial data or doing geoprocessing that are accessed through a desktop software and/or web application. Some examples of GIS software include QGIS, ESRI's ArcGIS, and Carto (as an interface to PostGRES and PostGIS)

**As a domain**, GIS is a realm of study focused on the development and application of geographic information systems for research purposes and/or for industrial uses. Here, people might be developing new algorithms to optimize things like geographic point clustering, route optimization, spatial geometry simplification, and more. Often times people contributing to GIS come from fields like computer science and engineering. 


### Remote Sensing

![NASA JPL - Aster image](https://asterweb.jpl.nasa.gov/content/03_data/05_Application_Examples/urban/fig3.jpg)
via [NASA JPL](https://asterweb.jpl.nasa.gov/content/03_data/05_Application_Examples/urban/default.htm)

Remote Sensing is really about the physics of light and how it interacts with features on the earth's surface or atmosphere. (Remote sensing is spectacularly interesting!). Remote sensing is about sensing from afar, whether that is taking images of the earth in the visible spectrum (think RGB images like those we can take on our phones) as well as "imaging" other wavelengths of light. People doing Remote Sensing study everything from physics to chemistry and how different wavelengths of light interact with features of interest - e.g. absorption of near-infrared and infrared is high for water whereas reflection of near-infrared/infrared wavelengths of light are high for plants. 
There are two types of remote sensing:
* [Active remote sensing](https://www.nrcan.gc.ca/maps-tools-publications/satellite-imagery-air-photos/remote-sensing-tutorials/introduction/passive-vs-active-sensing/14639) explores technologies like RADAR and LiDAR to actively sense the environment by producing the source of light or energy to sense what is in its **Field-of-View (FOV).**
* [Passive remote sensing ](https://www.nrcan.gc.ca/maps-tools-publications/satellite-imagery-air-photos/remote-sensing-tutorials/introduction/passive-vs-active-sensing/14639) is passive in the sense that it is only sensing light or energy that is reflected back to its sensors from its **Field-of-View (FOV).**


***
***
***

# Mapping Roadmap

This mapping roadmap is about meant to lay out some of the key technical skills that be involved in helping you with your mapping endeavors. 

This roadmap is divided into 4 sections:
1. Domain Knowledge
2. Front-end (TBD - not sure if this is the right name)
3. Back-end (TBD - not sure if this is the right name)
4. DevOps

* https://mapschool.io/

## Domain Knowledge

This is probably the most important thing of all. You gotta read! Embrace your inner nerd. Dork out on your interests. Watch movies. Educate yourself! Learn as much about a topic as possible. Knowing about the thing you're mapping (or learning about it on the way) is crucial. Your role as a mapper is to speak truth to power. The only way to do this is to know as much about the thing you're mapping as possible. 

Maps are a tool to help you understand something. Maps lie all the time because data lie all the time. We are shaped by our experiences (or ignorances) and the tools we use - e.g. statistics, discrete color choices, categorizations. The best thing you can do is to invest as much time (or more) into learning about some subject - e.g. pollution, music, literature, anything! - as you do learning mapping tools. The way I see it, if you can't can't explain in a reasonable way what you're rendering onto a map, you probably should be wary of publishing your maps. Additionally, if you're totally confident about your map, you should be questioning all the things that make you confident about your map - have you covered *all* your bases? Have you made sure your map doesn't have unintended consequences for you or for the people and places you're mapping?

***
***
***

## Front-end

I'm calling this the "front-end" since conceptually this part of the roadmap has more to do with the visualization or representational parts of mapping.

### Cartographic Fundamentals

I'm basically re-iterating what is outlined in the [Axis Maps - cartography guide](https://www.axismaps.com/guide/)

#### Symbology / Visual Variables

* https://www.axismaps.com/guide/general/visual-variables/


#### Projections

* https://www.axismaps.com/guide/general/map-projections/

Probably one of **the most important concepts** that a geographic education can emphasize. Having a handle on projection can save your sanity, save projects, and even save lives.

* [EPSG 4326 vs EPSG 3857 (projections, datums, coordinate systems, and more!), Lyzi Diamond, 2017](https://lyzidiamond.com/posts/4326-vs-3857)
* [Understanding Projections, Tom MacWright, 2012](https://macwright.org/2012/01/27/projections-understanding.html)

Some video content for the more visually inclined:
* [Why all world maps are wrong, Vox](https://www.youtube.com/watch?v=kIID5FDi2JQ)
* [Map Projections Explained - A Beginners Guide, Mango Map](https://www.youtube.com/watch?v=wlfLW1j05Dg)
* [Types of Map Projections, Mr. Sinn](https://www.youtube.com/watch?v=IBYzeT2O97g)
* [Introduction to UTM, Universal Transverse Mercator., GIS and GPS Tips & Techniques](https://www.youtube.com/watch?v=LcVlx4Gur7I)

#### Color & Maps

* https://www.axismaps.com/guide/general/using-colors-on-maps/

#### Scale & Generalization

* https://www.axismaps.com/guide/general/scale-and-generalization/

#### Labeling and text

* https://www.axismaps.com/guide/general/labeling/

### Reference Map Types

Reference maps are probably the first thing we think of when we think of maps. Reference maps are maps that are more about navigation and the locations of things. These could be maps that you might use for hiking that show the topography and the hiking trails in a national park or a tourist map of a city showing the the street plan and key landmarks.

### Thematic Map Types

I'm basically re-iterating what is outlined in the [Axis Maps - cartography guide](https://www.axismaps.com/guide/).

[Thematic maps](https://en.wikipedia.org/wiki/Thematic_map) are maps of a geographic area focused on "a particular theme or subject area." These themes or subject areas tend to represent some kind of statistical data or classifications. Thematic maps tend to represent **numerical** (anything countable or measurable), **nominal** (anything classifiable or nameable), or **ordinal** (anything that can be ordered relative to eachother) data.

* https://www.axismaps.com/guide/multivariate/multivariate-vs-univariate/

#### Choropleth maps

* https://www.axismaps.com/guide/univariate/choropleth/
* https://www.axismaps.com/guide/multivariate/bivariate-choropleth/
* https://www.axismaps.com/guide/multivariate/value-by-alpha/

#### Proportional Symbols

* https://www.axismaps.com/guide/univariate/proportional-symbols/
* https://www.axismaps.com/guide/multivariate/bivariate-proportional-symbols/

#### Dot Density

* https://www.axismaps.com/guide/univariate/dot-density/


#### Cartograms

* https://www.axismaps.com/guide/univariate/cartograms/
* https://www.axismaps.com/guide/multivariate/bivariate-cartograms/


### Web Mapping

These days the web is how most geographic data are visualized and published. Having a web mapping framework handy is crucial to having a means of increasing access to your map. Not all web maps need to be interactive and certainly web maps aren't always a replacement for a really good static print map, but web maps do offer a lot of possibilities for communication. 

* https://www.axismaps.com/guide/web/what-is-a-web-map/
* https://www.axismaps.com/guide/web/map-interaction/
* https://www.axismaps.com/guide/web/should-a-map-be-interactive/

#### HTML5

When we tak about web mapping, what we're really talking about is maps that live within the context of HTML/CSS/JavaScript. As [Lyzi Diamond writes](https://lyzidiamond.com/posts/geographic-education), learning tools is not enough. The concepts and general skills are central to proficiency in mapping. 

It is worth reading:
* [What should I learn first? pt.1, Lyzi Diamond](https://lyzidiamond.com/posts/what-to-learn-first)
* [What should I learn first? pt.2, Lyzi Diamond](https://lyzidiamond.com/posts/what-to-learn-first-pt-2)

Anyhow having at least some basic foundations in how web technologies work, what are APIs, how HTML/CSS/JS work together, differentiating between server-side and client-side programming, AJAX, databases, can dramatically change your experiences with web mapping. 

* The [ITP Dynamic Web Development Course 2020](https://github.com/itp-dwd/2020-spring) is a full-stack course introducing foundational skills.
* The [Full Stack Open Course](https://fullstackopen.com/en/) is excellent for the latest and greatest.

#### Pick a web mapping application tool

I will start by saying that I think tools like Excel and Google Spreadsheets are extremely powerful. For exploratory data analysis, having a sandbox within which to "play" and to discover is super important. Furthermore, having environments that have low overhead and intuitive interfaces is a major plus. 

Having a web mapping application tool in your "back pocket" that is reliable, powerful, and quick is a must IMHO. That being said, off the top of my head, my first go-to recommendations for web mapping applications would be:

Web mapping apps:

* [Kepler.gl](https://kepler.gl/)
* [Carto](https://carto.com/)

More generally:
* [rawgraphs.io](https://rawgraphs.io/)
* [DataWrapper.de](https://www.datawrapper.de/)

Some Specific Purpose Based Apps:
* [Knight Labs Story Map](https://storymap.knightlab.com/#overview)

#### Pick a web mapping framework

Web Maps are a clever construction. Having a general understanding of how they work (and their limitations) is important!
* [How Web Maps Work, Tom MacWright](https://macwright.org/2012/05/15/how-web-maps-work.html)

Pick one or two of these and learn them well. 

A lot of things are being built on top of MapboxGL so that is definitely worth spending some time with. 

* My recommendations:
  * [Leaflet.js](https://leafletjs.com/) // my recommendation to get started
  * [MapboxGL.js](https://docs.mapbox.com/mapbox-gl-js/api/) // Mapbox GL is powerful. Getting used to the GL context can be a transition, but their documentation is generally good.
  * [Google Maps API](https://developers.google.com/maps/documentation) // Google maps is undoubtedly one of the most powerful web mapping platforms out there. With access to APIs like streetview, google places search, and more, I have to say, it is very powerful. 
* For more advanced contexts and when you need to get out of the web mercator:
  * [D3.js](https://d3js.org/) // much more advanced but definitely offers a lot of opportunities to get out of web mercator projection.
* Other Options:
  * [Deck.gl](https://deck.gl/#/) // for those of you who are into React.js
  * [Carto.js](https://carto.com/developers/carto-js/v3/)

### Desktop GIS



***
***
***

## Back-end

I'm calling this the "back-end" since conceptually this part of the roadmap has more to do with data processing, analysis, and generally all the things that happen before you get to the visualization or representational parts of mapping. 

### Geographic Data


* [Odd Maps](https://macwright.org/2011/11/10/odd-maps.html)


### APIs

#### Static Imagery

* Mapbox static imagery
* Google static imagery

#### Routing

* Mapbox routing
* Google routing
* Graphopper routing

#### Placename Search

* Mapbox search and geocoding API
* Google search and geocoding API

#### Datasets

* Openstreetmap



## DevOps

I'm calling this the "devOps" since conceptually this part of the roadmap has more to do with the kinds of skills related to geospatial infrastructure. 


<!-- 
## Geographic Data

## Projections

## Geo Analysis

## Geo Visualization

## Cartographic Design

## Web Mapping

### Desktop GIS 
-->

<!-- 
# Everything Besides the Map

No one told me when I started getting into maps that basically mapping is about more than "just" putting things on a map. There's a whole "stack" of things that are not directly related to "maps" per se, but are totally essential for making mapping possible.

### Databases

### Full stack web development

### Statistics

### Data Visualization

### Domain Expertise 
-->


