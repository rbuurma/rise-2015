# Metadata for *Evelina* and Friends (Exercise 6)

+ Writeup due to Known before class Monday, November 2nd, 2015
+ Estimated time: 1-2 hours

In exercise 5, we moved from using digital text analysis tools to examining single canonical novels to thinking about how we might look at some successively larger sets of novels. We examined some bibliographic metadata in both printed bibliographies and ECCO, and we visually examined digital facsimiles of eighteenth-century novels and also used the ARTEMIS tools to analyze and explore the OCR'd text of those facsimiles and the metadata attached to them. (Metadata, you will remember, is just "data about data"; bibliographic metadata is data about books, for example the electronic catalog records that accompanied the ECCO facsimiles. The metadata of a Word or PDF document usually contains information about the author, the program used, the time and date of composition, etc.)

Now we are going to look in more depth at two elements: metadata (in this exercise) and full texts (in exercise 7). We will play with some metadata and practice modeling a collection of novels to see what more we can learn about early fiction in English using these methods before turning to experiment with how we might ask research questions that join metadata with full-text analysis (in exercise 8).

### Step 1: Look at the metadata.

You have a csv (comma separated values) file of selected metadata on about 855 novels published between 1700 and 1779. This hybrid metadata began its life in a library card catalog record, and was then exported and enriched with additional information by students working for the [Early Novels Database](earlynovels.org). This data was made by people and has been selected and pulled from an in-progress dataset; there will be errors! (If you are interested, here is a [more minimal set of metadata records for eighteenth-century novels](https://github.com/rbuurma/rise-2015/blob/master/Underwood_HTRC_fiction_metadata_1700s.csv) that exist in full-text digitized form in HathiTrust and as a subset of the HathiTrust Research Center [extracted features dataset]([https://analytics.hathitrust.org/features](https://analytics.hathitrust.org/features)) - scroll down to "sample files.")<sup id="a1">[1](#f1)</sup>

What does the collection of 855 novels described in these records represent? That's a difficult question. The novels (or, much more accurately, prose fictions) are all in English; they were all published between 1700 and 1779; and they are drawn from a few places: from Penn's Collection of British and American Fiction, 1660-1830, and from the Swarthmore and Bryn Mawr libraries, and from the Library Company of Philadelphia. To know how the novels represented in this metadata relate to the entire world of early novels in English published would require more research. But to give you some sense, we can take the 1760s as a sample decade. *A rough estimate  suggests that about 639 unique titles of prose fiction in English were published in the 1760s, and our END metadata set includes 132 of them, or about 21%.*

To get a first look at the metadata set, find the [exercise6ENDmetadata1700_1779](/Assignment_materials/exercise6ENDmetadata1700_1779.csv) file on our Github or in our Dropbox "Assignments" folder and download it. Click through to look at the file on Github or open the file with a spreadsheet program (Excel or similar) and look at it. You will see that each line is a set of metadata about an individual novel, and each column represents a value or metadata field. Here is a list of descriptions of each one:

****
+ OCLC - A number used for bibliographic control
  + AuthorName - Author's name, if known.
  + AuthorDates- Author's birth and death dates, if known.
+ Title - the full title transcribed from the first full title page.
+ PubLocation - The city in which the novel was published, transcribed from the title page.
+ PubDate - The date of publication transcribed from the title page.
+ Format - The book's format (more on this in class) - based on how many times each sheet has been folded to form each gathering.
  + VolumeStatement - Number of volumes the book declares on its first title page.
  + ParatextTitle - Standardized names of all existing paratexts aside from the title page and advertisements - prefaces, dedications, tables of contents, indexes. Note that a blank cell means that the book does not include any of these.
  + EpigraphBoolean- Does this work have an epigraph on the title page? 0=no, 1 = yes
+ NarrativeForm - The primary narrative form of the novel as determined by the cataloger. (Very subjective!)
  + NarrativeFormAdditional- Additional narrative forms in the novel as determined by the cataloger.
+ NonProseForms - Poems? Sheet music? Other non-prose forms, as determined by the cataloger?
+ InscriptionBoolean- Does this work have an inscription (the name of a person, usually an owner) on the title page? 0=no, 1 = yes
+ MarginaliaBoolean - Does this work contain any marginalia (writing in the book)? 0=no, 1 = yes
+ TranslationClaims - Claims about the text's being a translation, abridgment, or adaptation made on the title page or in the paratext, regardless of actual status of the text.
+ CatalogedBy - The name or initials of the student researcher who created most of the metadata in the record.

*The following are lists of words or phrases appearing in the full title, as it appears on the novel's first title page.*

+ TitleOtherWorks - Titles of other books included on the title page, often as part of an author statement, ie, "*Pride and Prejudice*, by the author of *Sense and Sensibility*."
+ TitleNouns - Nouns in the title.
+ TitleAdjectives - Adjectives in the title.
+ TitlePlaces - Place names in the title.
+ TitleNames - Names of people in the title.
+ TitleVerbs - Verbs in the title.
+ TitleObjects - Material objects referenced in the title.
+ TitleAdverbs - Adverbs in the title.
****

Note that your spreadsheet program is already a type of data visualization, though a very general and not especially useful one for our current goal of exploring this dataset. What we need is a way to easily select one or a few of the columns and visualize their values.

### Step 2: Google Fusion Tables

First, we will use Google Fusion tables, which is a relatively simple way to take a spreadsheet of information and create some visualizations from it. Go to www.google.com/fusiontables, sign in with your Google account (create one if you don't have one), and find and upload the exercise6ENDmetadata1700_1779 file. Choose "comma" for "separator character" and "UTF-8" for "character encoding" if they are not already chosen as default. Then click "next." You will get to a file that will show you a preview of the table; at the top, for "column names are in row" make sure "1" is chosen. Click "next." In the next window, uncheck "allow download" and attribute the data to "The Early Novels Database." Click to finish and everything should finally import.  (To get the most out of this exercise, consider viewing some of the Fusion tutorials before moving on the explore the END metadata.)

*Note: please do not make your table public. If you want to share it with someone, use the sharing settings to generate a link that allows people with the link to view the table, and check the box preventing viewers from re-sharing.*

After you have created your table, you will see some tabs. In the first tab, you will find a spreadsheet. Each row represents a record of a different novel. Each column represents a different metadata field. *These are just a selection of fields pulled from a larger, messy, in-process metadata set; some of them will be more interesting than others. Some will be interesting but you will discover are not yet in a form you can use given your existing tools.*

Most of the columns will define their data type as "text," but you may wish to modify these. To do this, use the drop-down menu at the top of the column to select "change" and then change the "type" to the best form. For example, probably PubLocation and TitlePlaces should be set to "location" if they aren't already, "PubDate" should be "date-time," etc.

Explore the data in the cards, which take each row - each record of a novel - and display them in a card catalog style.

#### Map (optional)

Click the red "+" to create a new tab. Make a map or maps of PubLocations or TitlePlaces if you want. If you do this, note that geolocating the placenames will take a little while.

#### Graph

Click the red "+" to create a new tab. Choose the bar graph graphic on the left. Under "category" choose "PubDate" and check the "summary" checkbox. Scroll down and set "maximum categories" to 100. (Note that the maximum number is 100.) On the "sort by" drop down menu, choose "PubDate." What do you see? Now choose the "filter" dropdown menu and filter by categories of interest - try some of the different values of "narrative form," for instance.

Click the red "+" to create a new tab. Choose the pie chart on the left. Under "category" choose "NarrativeForm" and check the "summary" checkbox and make sure the "Value" is set to "count of Narrative Form." Scroll down and set "maximum categories" to 15. What does this visualization tell you?

What other visualizations can you make using Fusion tables and the data in its current form? Try some.

What can't you do in Fusion Tables with the data in its current form? For example, I might want to trace the occurrence of books with prefaces over time - as both raw numbers and as a percentage of books in the collection for any given decade - but I would have to transform this data in order to do that. (What would I need to do?)

### Step 3: Word cloud

The set of fields that break down the novels' titles are text data rather numerical data; while we could do some counts of them in Fusion, perhaps a visualization tool better suited to a collection of words, like a simple word cloud, would make more sense.

In Excel or another spreadsheet program, copy the column you are interested in. Paste it into TextWrangler, Notepad++, or a similar program. Using the "find a replace" function, find all of the commas and replace them with one blank space.

Copy the resulting words (the extra spaces won't make a difference) and drop them into www.jasondavies.com/wordcloud or another wordcloud generator of your choosing.

### Step 4: Write

Write a few paragraphs about what you have learned about this metadata and the set of novels it describes. What were you able to learn about this dataset? What would you have liked to learn about the existing data but were unable to because of the data's form or the tools you had? If you had more tools or more data (either different types of metadata or more metadata or both), can you imagine research questions you would like to ask? Have you learned anything, large or small, about the process of visualizing and analyzing metadata? Post to Known with #Exercise6 #metadata and anything else you would like to add.

### Remember

This is the first iteration of this assignment; if you run into bugs or other difficulties, please let me know. 

----------

<b id="f1">1</b> Boris Capitanu, Ted Underwood, Peter Organisciak, Sayan Bhattacharyya, Loretta Auvil, Colleen Fallaw, J. Stephen Downie (2015). Extracted Feature Dataset from 4.8 Million HathiTrust Digital Library Public Domain Volumes (0.2) [Dataset]. HathiTrust Research Center, doi:10.13012/j8td9v7m. [↩](#a1)
