# NYC Islandora Meeting: May 2019
* **Date:**  May 7, 2019
* **Time:** 3 - 5PM
* **Location:** Milstein Center 402, Barnard College

* [NYCIslandora Google Group](https://groups.google.com/forum/#!forum/nycislandora)


## ATTENDEES
Please add your name.

* 

## AGENDA
* Welcome & Introductions
* Updates and current projects

## NOTES
Thomas / LaGuardia
* Have islandora up and running at laguardia!! took about a year and a half, on and off
* Trying to find a cms for digital archives at cuny—looking at omeka — lots of complicated different scenarios at different places
* Mostly adding oral history materials, publications, photos
* Using pdf viewer for the publications, but having issues with slow loading -- it's an issue with the pdf viewer javascript--tries to load the entire item before showing anything
* Will be debuting it at a CUNY-wide presentation day on different platforms: ArchivesSpace, Omeka, Islandora, a video thing, and DuraCloud. 

Robin and Andrea / NYAM
* Working on enhancing metadata for last collection uploaded -- the Ladd collection
* Won a prize for Facendo Il Libro collection! Covers the entire lifecycle of a digital collection -- applying for grant, mockups, in-house digitization. 
* Trying to build a design for the comparison display of different texts--would want a true IIIF viewer rather than the compound object
* Instead of straight HTML, could use more like a view, thinking about other ways to go about it. Perfect as the enemy of good!
* Planning a usability study
* Migrating their last collection from ContentDM - the Resurrectionists. Not using the API. Trying to think about how to reconstitute the collection, rather than just copying everything over. Also thinking about re-scanning. Is disparate objects, but they were bound together. 

Karen / METRO
* Harvesting collections, doing some batch edits
* How does everyone do find and replace? Using the module (updated by Diego to include regular expressions)? Other ways?
* Henry uses a method to generate PIDs using Solr and then does updates using spreadsheets/multi-importer
* Now the find and replace is being maintained 
* Merging research on linked open data, wiki data into the Archipelago project. Spinoff group of Linked Data for Production -- Wikidata affinity group. Can share info for the group--calls every two weeks with case studies.
* Wiki education is doing a one/two-day workshop on Wikidata for libraries. Wikidata is making a big push in being incorporated into the internet. Much more open than other controlled vocabularies. Less resistance than before from larger vocabularies (e.g. Getty, OCLC)
* A little bit different than typical semantic ontologies--just more open
* Summit on wikibase--now it's easier to download

Henry, Jerome, Al / NY-Historical Society
* Working on multiple digitization projects - subway construction photos, got an NEH grant to finish that work. Doing a lot of ingesting
* Money from Leon Levy foundation to work with born digital materials
* Working on pulling in museum collections to Islandora. Museum data is in TMS
* Had originally been trying to ingest everything and create metadata that would work for both collections. Now the approach is to get some reference objects. eMuseum uses Solr, can just pull from both Solr stores.
* Bring in object image and ID--use as identifier, just use Islandora as the skin. Definitely keeping TMS, since the museum system uses it a lot. But museum does like the idea of having a unified search system
* Islandora 8 - looking at migrating

Martha / Barnard
* Bootstrap refactoring of the digital collections - work is slowing down and trying to hand off to vendor - Diego can share a bootstrap theme (on 3)
* Ingesting new collection of recordings using oral history solution pack
* ICG - having an ISLE/LASIR (and some migration/Islandora 8/roadmapping stuff) hack/doc in Troy, NY - May 23-24th - more info [here](https://islandora-collaboration-group.github.io/icg_information/hack_docs/RPI/)
* CoC review for Islandora foundation - please fill out the the [survey](https://docs.google.com/forms/d/e/1FAIpQLSfwaj4kCLr6UwBdUD4oyRSGwtrHpYgJqJcnrYXl_Drg61xH7g/viewform)! Note about language justice

Diego / METRO
* [Archipelago Commons](archipelago.nyc)--attempt to rethink what a repository should be 
* Islandora 8 is too complicated to deploy/use, didn't feel sustainable
* What is most important? Metadata - consistent experience for adding, editing, using metadata. Drupal thinks of metadata in a very flat way--flat lists of fields with hierarchies, limitations to fields, no possibilities for linked open data
* Need to rethink metadata. Building a system that doesn't rely on schemas.
* Built on Drupal 8, database, Solr, and cantaloupe image server. Everything runs on Docker and uses Amazon S3 storage (with Minio possibility). 
* Uses Drupal 8 as a microservice.
* Not storing derivatives--Cantaloupe produces them in real time. Cantaloupe caches, but reduces the overall storage.
* Docker means easier development, just develop over the Docker compose
* Cantaloupe can interact with pdfs, extract video frames, etc. 
* StrawberryField - field that deals with data in json. Takes a full json blob. Metadata never needs to change, can just get displayed/indexed in different ways. Uses Twig to generate html/xml/json on the fly.
* Webforms - build a form however you want, StrawberryField understands how you want it to use.
* IIIF viewers are enabled - bookreaders, panoramas, annotations, etc.
* Twig template renders metadata in whatever format (e.g. a block, with whatever labels)
* Only two kinds of objects -- digital object and collection
* Added part in the workflow to add linked data--pulling from LoC API
* Wikidata doesn't really have "preferred terms" in the same way--can change the label, do whatever you want
* Can generate a stub wikidata entry through the interface if some value doesn't exist
* Tools in development for updating data based on updates in vocabularies
* Can decide on the viewer/display per object, or by rdf type of object
* Generating schema on the fly--generates structure. Also creating tools to be able to edit the 
* Hashtag based structure in the storage?
* Will be refactoring multi-importer for it
* Road map is on the [github](https://github.com/archipelago-commons).
* Currently supported by METRO. 3-year community building project, then METRO will stop being the architect. 
* Will move DCMNY to Archipelago, probably over next year
* Searches, collection membership, exhibits--all views
* Handling migrations - keep center star information forever, just reshape as context evolves. Can just dump any json in along with files (this is planned). Can also move json out
* Multiple ways to edit the metadata--just the content, or the entire fields
* Preservation gets pushed to the storage side--S3
* Can scales up--one field per object, so a million objects is a million fields.
* Not a replacement for Islandora, something different
* Collection membership is not enforced--objects don't have to be 
* Add use cases to the [google group](https://groups.google.com/forum/?utm_source=digest&utm_medium=email#!forum/archipelago-commons)!

