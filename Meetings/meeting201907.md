# NYC Islandora Meeting: July 2019
* **Date:**  July 16, 2019
* **Time:** 3 - 5PM
* **Host:** The New York Academy of Medicine
* **Location:** 1216 5th Avenue, New York, NY 10029 (3rd floor)

* [NYCIslandora Google Group](https://groups.google.com/forum/#!forum/nycislandora)



## ATTENDEES
* Deena Schwimmer, Yeshiva University
* Margo Padilla, New-York Historical Society
* Henry Raine, New-York Historical Society
* Albert Min, New-York Historical Society
* Diego Pino Navarro, Metropolitan New York Library Council
* Karen Hwang, METRO Consultant
* Thomas Cleary, LaGuardia Community College
* Andrea Byrne, New York Academy of Medicine
* Robin Naughton, New York Academy of Medicine


## AGENDA & NOTES
### Welcome & Introductions
* Deena Schwimmer is working on launching Islandora for Yeshiva University Archives.  This is her first time at the group.
* Margo Padilla has joined the New-York Historical Society and this is her first time at the group.

**Discussion & Questions**

Deena brought some great questions regarding Islandora and some of the issues she's encountering.
* Date faceting - date range not working correctly.
  * Ticketing system doesn't have anything at this time about date faceting.
  * Dates are multi-value fields in SOLR.  
  * Diego fix for San Diego State - can share with Deena and vendor. Solr side - always fixes.  Notify the community.
  * Format the dates - Islandora allows you to format into human-readable string.
* Sub-collections - counting all collections but believe there are only six collections with many sub-collections.  The intellectual vs. digital definitions of collection differs.  
  * Could add into the metadata "sub-collection"
  * Index hierarchy
* Multi-importer (IMI) - what's the workflow.  
  * Suggestion: If you make corrections in Islanodra, make corrections in spreadsheet.  Changes in Islandora can be overwritten with a new import.
  * You can ingest and update objects.
  * If you have access to Solr you can export the items back into spreadsheet.  
  * It's not automatic to get pipe in the data, but you can add the information during the Solr  export.
  * Is there a way to do a batch ingest that will look at new data and not old?  No.

### Possible Workshops
* TWIG
  * Could use this meeting to test doing a twig workshop.
  * Every programming language has a method so could potentially provide and view into creating usable templates.
* OpenRefine (basic and advanced)
  * METRO has offered OpenRefine workshops in the past.  If done by METRO, it will need to be free. Becoming a METRO Meetup may be an option.  Instructors need to be compensated.
  * Karen could teach it.
* MODS - can learn about MODS else where.  Lots of others can talk about it outside this group.  
* XML Forms possible - Diego has a workshop that we could use.
* Archipelago
  * Want to show what it can do.
  * First official release will happen at the end of the year. There are already test downloads and use.
  * Islandora migration (Islandora 7 to 8) will need to happen by 2021.  
   * Fedora 3 is dead and Fedora 4 usage is slow.  The big institutions never migrated to Fedora 4 and it's possible that Fedora may be consumed by Lyrasis.
    * Drupal 7 & 8 will be done at the same time.  Drupal 9 is coming.
* Good habits/methods for working with data
This topic covers a lot of areas and information.  One discussion point was creating a proposal for a METRO series, which can include multiple workshops.
  * Create a page where we can discuss ideas about workshops.
  * Potential Audience: Small & large institutions, individuals, information professional groups
  * Preparing your data for ingest
    * Quality of the data
    * Constraints
  * Tools - OpenRefine; Excel; CSV; parsing json; getting data from other systems; data formats and character;
  * Editing data once in Islandora.
  * Other systems: ContentDM; Omeka
* SOLR - facets
* Digital Preservation workshop
* Davis (METRO) reached out to a  colleague regarding survey about what workshops people want to do.


### Actions
* Propose a group of workshops to METRO
* Create a place to work on developing workshops. ([Completed - link to NYCIslandora Wiki Workshop Page](https://github.com/rnaughtonwk/NYCIslandora/wiki/Workshops))
* Create a place for glossary   ([Completed - link to Google Glossary Document](https://docs.google.com/document/d/1lKFPX1qtCcaGi2x6RK4gaIJrzVPnS1Ae4CFYV1yHtcs/edit)) 
  * Should determine if to move glossary onto the wiki or leave in Google Docs.
* Useful links page.([Completed - link to NYCIslandora Wiki Resources Page](https://github.com/rnaughtonwk/NYCIslandora/wiki/Resources))

### Updates & Current projects
* Karen - finished migration project.  Working on migration 327K objects; 66 collections; Using API to gather data - Compound with only one child. May need to consider alternative
* Thomas - will be traveling
* Henry - continuing to work on ingest
* Diego - migration; islandora release; internet book reader; good community feedback; Archipelago; documentation  - goal groups
* Albert - helping Henry figure out way to ingest a large group of images (subway) on the server - Minio server (s3) recommendation.
