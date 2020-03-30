# A1: Scavenger Hunt

- [A1: Scavenger Hunt](#a1-scavenger-hunt)
  - [PREREQUISITES](#prerequisites)
  - [READINGS](#readings)
  - [BRIEF](#brief)
  - [Requirements](#requirements)
    - [Part 1: Selecting a Subject](#part-1-selecting-a-subject)
    - [Part 2: Begin - Observation](#part-2-begin---observation)
    - [Part 3: Export a GeoJSON of your findings.](#part-3-export-a-geojson-of-your-findings)
    - [Part 4: Begin Research](#part-4-begin-research)
    - [Part 5: Documentation](#part-5-documentation)
  - [Submission](#submission)

## PREREQUISITES

Before you continue, read the [final project briefing](final-project.md). 🙏

## READINGS

* See: [Week 1 - Readings](../BIBLIOGRAPHY.md#week-01-everything-is-spatial)

## BRIEF

This week your assignment is to begin observing the environment using @joeyklee's [Streetview Mapper](https://streetview-mapper.org) - a web app that allows you to explore Google Streetview and map what you see to a shared public database. Your task will be to **define ONE subject/phenomenon of interest** and catalog it with the Streetview Mapper and **add hashtags** and **descriptions** to your findings. This practice will continue throughout the duration of the course; the data you collect will be central to grounding the theoretical and practical aspects of this course.

The point of this observational experiment is to train you to focus your attention. Throughout the course, you will be challenged to simultaneously observe and unpack your subject's varying characteristics and qualities and, more interestingly, the subject's history, politics, and geography.

This week, your task is to choose one subject/phenomenon of interest and be meticulous about collecting photographic/geographic evidence of it. There are key constraints to the subject you select, listed below:
* You **may not**:
  * violate the privacy of another person - surveilling without permission is not permitted.
  * choose a subject that will put yourself or another person in danger.
  * do anything illegal 
* You **may**:
  * select a seemingly "simple" subject (simple topics will inevitably lead to complexity, no doubt!)
  * "observe" from afar - if you are particularly passionate about "remote sensing" or remote data collection - your data collection/"paying attention" may take the form of collecting imagery of a specific subject using the web or other platforms.


## Requirements

### Part 1: Selecting a Subject

Choose a subject to observe and write about it. 

Some ideas:
* Stolen bikes or evidence of stolen bikes
* Broken sidewalk infrastructure
* LinkNYC Booths
* Bus Stop Infrastructure
* Telephone Poles
* Vegetation
* Street-side trash bins
* Fire hydrants
* Manhole covers
* Shop signs 
* Link NYC kiosks
* Bus Shelters
* Street Trees
* Security Cameras
* Empty tree beds
* Graffiti
* Trash bins
* Subway Entrances
* Bodegas
* People's Clothes

Some methodological considerations:
* [Paying attention guide](../guides/paying-attention-guide.md)

### Part 2: Begin - Observation

Define a method for your observations and begin data collection. 

It is important that in this step you do THREE things:
1. Define your rules on what is considered "valid" data (e.g. If we're collecting data about street-side trash bins, do recycling bins also count?)
2. Be meticulous about your data collection. Collecting data willy-nilly is one approach, just be meticulous about your "willy-nilly-ness". You can also consider more systematic approaches. You will need to consider the **spatial distribution** of your subject of interest - e.g. it probably doesnt make sense to map storefront signage in residential suburbs. One approach would be to define a neighborhood to start in and systematically approach your collection street-by-street. 
3. Your data must have at least:
   1. One `#hashtag` that will make your project identifiable. Preferably additional hash tags would be added. This is what you'll use to filter through your data collections later on so make sure to tag your images!
   2. A description of what you have mapped. In case you have observations worth sharing, describe what you're seeing.


### Part 3: Export a GeoJSON of your findings.

In the Streetview Mapper, navigate to the [Dashboard](https://streetview-mapper.org/dashboard). There you can see all of the locations you've saved to the database. 

Here you will do 2 things:
1. Take a screenshot of your dashboard with the full extent of all the points you've mapped.
2. Export all of the data you've cataloged during the week. You can do this by pressing the large green button that says, "**export to geojson**." This will export and save a file called `streetview-mapper__TIMESTAMP.geojson` where `TIMESTAMP` is the Unix timestamp when your data were exported. We will talk more about GeoJSON files and spatial data formats next week.

**Optional**:
You can plot them onto [GeoJSON.io](http://geojson.io/#map=2/20.0/0.0) by simply *dragging and dropping* your newly created `streetview-mapper__TIMESTAMP.geojson` file into the GeoJSON.io website. Notice in the **right panel** you can see what your data looks like. Particularly of interest are the properties of the geojson that separate the **geometry** from the **properties** of each **feature**.


### Part 4: Begin Research

By now you will have spent some time exploring Streetview and observing instances of your subject of interest. Depending on what you've decided to study, you might on one hand be learning/thinking about that subject for the first time or on the other hand you will have a deep, long history with that subject. Either way, this part of the assignment is to begin researching your subject and articulating your knowledge and findings. 

You will use the [Implosion Methodology](https://journal.culanth.org/index.php/ca/article/view/ca29.2.09/301) to create a "map" - not the geographic kind, but a conceptual one - of the dimensions of your subject. 

In this step, your goal is to go through 14 dimensions of researching a subject to help answer *How Is the World in “It” and How Is “It” in the World?*. You will try your best to answer the questions associated with each of these dimensions as articulated in the [Implosion Methodology Article](https://journal.culanth.org/index.php/ca/article/view/ca29.2.09/301). Try to limit this to a maximum of 1hr. The point here is that this will provide you with a valuable framework for knowing what you know, acknowledging what you do not, and providing a roadmap for what you might discover throughout the process of mapping:
* Labor dimensions
* Professional/Epistemological dimensions
* Material dimensions
* Technological dimension
* Context and situatedness
* Political dimensions
* Economic dimensions
* Textual dimensions
* Bodily/organic dimensions
* Historical dimensions
* Particle Dimensions
* Educational dimensions
* Mythological dimensions
* Symbolic dimensions
 
You will share the results of your "implosion" in your weekly blog post as described in the next step.

You can use the [Implosion Project Template](templates/implosion-method-template.md) to try to answer as many questions as possible.


### Part 5: Documentation

As part of your week 1 documentation you will submit the following:
1. A blog post that:
   1. **Clearly introduces the subject of urban media you will be studying**: e.g. "For my project, I will be focusing my attention on **street trees**. I define street trees as being..."
   2. **Clearly explains your methodology for data collection**: e.g. "I will be collecting data about **street trees** using Google Streetview. As part of the data collection on **street trees**, I will also collect locations where a tree bed exists but where no tree currently exists. I will start in the Park Slope neighborhood in Brooklyn, then work towards completing Crown heights, then..."
   3. **Clearly shows that you have started to collect data about your subject**. e.g. "In 1 week, I have collected 60 street tree locations. Here is a screenshot of my progress..."
   4. **Clearly shows that you have begin your research using the Implosion Method as described in step 5**

Be sure to note any questions you may have about terminology that you've come across, any concepts that seem confusing, or any technical issues you've encountered. 


## Submission

You will submit a link to your blog post to the link below, specifying which assignment you are submitting:

↳ 💌 [Google Form Assignment Submission](https://forms.gle/1tAfHZXEejZDubHg9)



<!-- 
* Paying Attention: collect data about 1 thing - use your camera phone to collect spatial imagery, organize, annotate, tag, and reflect on what you're seeing. ==> studio time for collecting coordinates.
 -->

<!-- 
*   * A1: Paying Attention - assignment is about paying attention: defining a phenomenon to map and observe, learn about, investigate, and report on.
    * this can be remotely done using aerial images 
    * or physically based (preferred)
* collect data about 1 thing - use your camera phone to collect spatial imagery, organize, annotate, tag, and reflect on what you're seeing. ==> studio time for collecting coordinates. 
* -->


<!-- As with any research, it is time to do some reading, watching, and digging. 
1. To start, try doing a web search (in your preferred search engine) and seeing what comes up with you put in, for example: "New York city bus stop" or "Hong Kong protest sites" or "Chile public space." You might append additional search terms like: "geography of" or "history of" or "analysis of" etc. 
2. Another starting point would be to examine the academic literature. You can search popular academic article search engines such as (note you will have to VPN into NYU or sign in to your account):
  - The NYU Library
  - Google Scholar
  - or any of [these search engines listed on Wikipedia](https://en.wikipedia.org/wiki/List_of_academic_databases_and_search_engines)

As you research, begin to organize your findings, take ample screenshots, and keep track of quotes and references you find useful or meaningful. 

If you've not done the reading, this is also a good time to do so. In particular, **Deep Mapping the Media City** and **Gaps in the Map: The Topologies of Cartography** by Shannon Mattern will help to frame our methdological approaches to the research we are conducting; we use maps and mapping (cartographic methods) as our tools to "excavate" the histories and stories our media subjects might tell (media archaeology). -->

<!-- 
Create a project folder and set it up such that you can keep your data and observations tidy. Document your images in a blog. Add any relevant annotations and notes, reflections, and questions that might be starting to arise about the subject, the methodologies, and anything else that comes to mind.

* Key questions:
  * ...
  * ...
  * ...

Additional Methodological considerations:
* [Googleform guide](../guids/../guides/google-form-guide.md) 
-->

<!-- 
While you're documenting, it is worth thinking about:
* **Articulates at least 3 questions or reflections about**:
   1. The usage of Google Streetview as a data source and mapping platform.
   2. The subject your are studying and what you are curious to discover
* **References at least 3 primary or secondary resources** - articles, videos, interviews - about your subject of interest. 
* 
* -->



<!-- 
Create a spatial dataset, specifically a `geojson` file from your images. Open that geojson file in [geojson.io](http://geojson.io/), a web service that allows you to easily view and make geospatial data, to visualize your data.

* **Automated** process: Ideally you can automate this process by using [img2meta](https://github.com/joeyklee/img2meta) to create a `.geojson` dataset from a folder of images (use the `true` flag). With the `img_metadata.geojson` you can drag-and-drop it into [geojson.io](http://geojson.io/).
* **Manual** process: Otherwise, there are analog methods for retrieving the metadata from your images as seen in [How to See an Image’s EXIF Data in Windows and macOS, How-To Geek](https://www.howtogeek.com/289712/how-to-see-an-images-exif-data-in-windows-and-macos/) in which you can create a `.csv` file or spreadsheet where you can manually create your data. Notes on structuring your spreadsheet data as a CSV and converting it to geojson can be found in the [CSV to GeoJSON Guide](../guides/csv-to-geojson-guide.md). 

-->