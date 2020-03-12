# Data Documentation Guide

This is a guide about how to document your data.

## Overview

Data documentation begins before you start collecting data and continues throughout the process of collecting data. Inevitably, there are always details about your collection that are important that emerge as you go about your data collection activities. These details could be to note how different events might have influenced your data collection (e.g. a parade or a pandemic virus, wink wink) or weather or device details can be crucial for the audience who might eventually use your data. 

This is a short guide on creating some awarenesses for you while you collect data in this class and in your other projects.



## README

When "shipping" or sharing data, you will want to include metadata that describes your dataset. These details include who created the data, when the data was created, how the data was created, if the data were derived from another source, any assumptions that have been made during the data collection that speak to the "truthyness" of the data, if the data has a "due date", and so on. These details are crucial for others to know how to use and understand your data. 

Here is a template for essential information you may want to include in your data's README:

* **Overview**:
  * **Title**: *Name of the dataset or research project that produced it*
  * **Creator**: *Names and addresses of the organization or people who created the data*
  * **Identifier**: *Number used to identify the data, even if it is just an internal project reference number - if you publish to an open data portal like Zenodo or Pangea they will assign you a DOI (document object identfier)*
  * **Dates**: *Key dates associated with the data, including project start and end date, data modification data release date, and time period covered by the data*
  * **Subject**: *Keywords or phrases describing the subject or content of the data*
  * **Funders**: *Organizations or agencies who funded the research, if any*
  * **Rights**: *Any known intellectual property rights held for the data - see LICENSE below*
  * **Language**: *Language(s) of the intellectual content of the resource, when applicable*
  * **Location**: *Where the data relates to a physical location, record information about its spatial coverage, the relevant spatial scales, aggregation levels*
  * **Methodology**: *How the data was generated, including equipment or software used, experimental protocol, other things you might include in a lab notebook*
* **Data Properties**:
  * `<key>`: `< String | Number | Boolean | etc >. description of the expected values`
  * `<key>`: `< String | Number | Boolean | etc >. description of the expected values`
  * `<key>`: `< String | Number | Boolean | etc >. description of the expected values`
  * ...

In the **overview** you can describe details about your data and in your **data properties** you can describe the properties within your data (if relevant or possible).

## LICENSE

You may want to include a license in your data. 

I would probably go for something that requires attribution. You can see some examples here at the [Open Data Commons Licensing](https://opendatacommons.org/licenses/index.html) page.

In the root of your data folder, I would include a copy of your selected license in a text file. For example, if I were to select the [Open Data Commons license with Attribution](https://opendatacommons.org/licenses/by/1.0/index.html) I would copy all of that license text into another file and save it my data folder and refer to that file in the README above.

Other things to think about would be potentially thinking about non-commercial licensing or other restrictions on your data usage. 

## Data Storage 

There are many services that allow you to share your data openly. Many of these are listed in [Nature's Open Data Portals Overview](https://www.nature.com/sdata/policies/repositories) 

* [Pangea](https://pangaea.de/)
* [DataOne](https://www.dataone.org/)
* [FigShare](https://figshare.com/)
* [Zenodo](https://zenodo.org/)

## References

* [Documentation and metadata, MIT Libraries](https://libraries.mit.edu/data-management/store/documentation/)
* [Metadata and documentation, U. of Leicester](https://www2.le.ac.uk/services/research-data/old-2019-12-11/organise-data/metadata)
* [Open Data Commons Licensing](https://opendatacommons.org/licenses/index.html)