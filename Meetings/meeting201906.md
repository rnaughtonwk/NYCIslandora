# NYC Islandora Meeting: May 2019
* **Date:**  June 11, 2019
* **Time:** 3 - 5PM
* **Location:** METRO

* [NYCIslandora Google Group](https://groups.google.com/forum/#!forum/nycislandora)


## ATTENDEES
* Karen Hwang, Metropolitan New York Library Council
* Diego Pino Navarro, Metropolitan New York Library Council
* Henry Raine, New-York Historical Society
* Albert Min, New-York Historical Society
* Jerome Tan, New-York Historical Society
* Robin Naughton, New York Academy of Medicine

## AGENDA
* Welcome & Introductions
* Goals & Plans
* Action Items
* Updates and current projects

## NOTES
### Possible Workshops
We discussed workshops that would be valuable to the team.
* TWIG
* OpenRefine (basic and advanced)
* MODS
* Archipelago
* Good habits/methods for working with data

### Updates & Current projects
### Karen
* Working on book object migration out of ContentDM into Islandora
* Merging the XML and CSV export for the data (XML to retrieve the page names)
* Using the CONTENTdm API to retrieve images

### Robin
* Migrating The Resurrectionists  collection from CONTENTdm to Islandora.  
  * The collection is small in terms of content and the team is working on putting the context back into the records/collection representation with the migration.
  * Table of Contents UI style design/new navigational elements
* User research study of the digital collections website.

#### Thomas
* Used ISLE for new instance of Islandora on AWS; Next step is to see how well it will integrate with CUNY OneSearch (primo - search all the libraries)
* CUNY trying to figure out hosting platforms for archives so that the archives could do a shared hosting; Thomas will be presenting Islandora as an option in the Fall along with other CUNY presentations on JStore; Omeka, etc..  

#### Henry
* A lot of ingest as usual
* Seeing things that could be improved with the multi-importer
  * Diego suggested opening an issue in GitHub.
* Ingesting with multi-importer failing but the cause is unclear.  
  * Diego suggested uploading the files to the server and telling the multi-importer to read the files from the server, then delete once imported.
  * Thomas asked about ISLE installation and ISLE can do something similar.

#### Albert & Jerome
* Working on redesign - highly customized viewer that's separate from Islandora.  
  * Looking at how we'll do that and what we need.  Have rest API endpoints; images going through cantaloup
  * Want access to Fedora directly
  * Islandora on its own doesn't give you the tools.  
  * Diego discussed Islandora IIIF  - Github - Adds layer on top of Islandora and converts to IIIF manifest  - [https://github.com/mnylc/islandora_iiif/tree/7.x-dev-presentation](https://github.com/mnylc/islandora_iiif/tree/7.x-dev-presentation) - use the 7.x-dev-preseentation branch.

#### Diego
* Archipelago
  * Roadmap - [https://github.com/esmero/archipelago-aws-demo/issues/6](https://github.com/esmero/archipelago-aws-demo/issues/6)
  * keep track in the taxonomy of all the metadata.
  * Why Drupal?
    * Can reuse pieces that require a lot of code.
    * Things that we don't like, we're re-developing and keeping in-house
    * Islandora users are used to Drupal.
    * Generates JSON
  * Migration - Archipelago read directly from the server
* Gatsby (https://www.gatsbyjs.org/) build the website based on JSON and never deal with coding the interface.
* Annotation tool - pass data and get the annotations; name entities, dbpedia, Wikidata,etc.   Can also submit JSON.
  * Humans still need to confirm what is correct when there are multiple items that are the same.
