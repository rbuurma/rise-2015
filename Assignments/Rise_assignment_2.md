# Mapping *Robinson Crusoe* (Exercise 2)

Here is a digital facsimile of a map from "The Farther Adventures of *Robinson Crusoe," also included in the fourth edition of *The Life and Strange Surprising Adventures" (click to enlarge):

![Farther Adventures map](http://pierre-marteau.com/editions/1719-robinson-crusoe/illus/1719-rc-vol-2-map.png)

In this exercise, we will create a simple visualization of the "Location" data you generated as part of Exercise 1 last week using the Stanford NER, which we will then compare with *Crusoe's* map.

There will be at least two interesting results. First, visualizing the NER-extracted locations on a map will give us a chance to make new interpretations of that data, and to compare those interpretations to those we were able to come up with by reading the "Locations" list. Second, there will be a number of locations that our technique will not be able to map. This will 1) help us think critically about our tools and technique but also 2) help us think a bit about fictional vs referential locations in *Robinson Crusoe*. (We'll also want to keep the latter results in mind for potential comparison to later fictional works as the semester progress.)

## Mapping *Robinson Crusoe* using Google My Maps

The steps are simple.

1.  Create a new copy of the data for this assignment.

2.  Using TextWrangler or a similar text editor, de-duplicate your NER "Locations" data if you haven't already. (If you had trouble with generating the NER data or if you rashly discarded it, I have included both raw and a de-duplicated versions of the NER "Locations" list in our repository.) You can also further clean it, if you want to, by manually deleting errors. (This will be somewhat subjective; that's necessary and fine.)

3.  Now you need to remove the "LOCATION" tags to avoid confusing My Maps. To do this, open the "find" box or similar find-and-replace function. In "find" put everything between the quotation marks here (the word LOCATION, the colon, and a space):

>  "LOCATION: "

In "replace" make sure that there is nothing (not even a space).  Click "replace all." Note that you can always use the "undo" function if you do something by accident.

4. Add a first line named "Location" at the very top of the document; this will become your My Maps column name.

5. Save your file with a .csv extension. (This stands for "comma separated values" and will let My Maps read each line as a separate value.)

6. Go to [Google My Maps] (https://www.google.com/maps/d/) and click "Create a New Map."

7. In the box on the left, select "Add layer" and choose the "Import" option to import your list of locations.

8. In the "Choose columns to position placemarks" pop-up box select "Locations" (or whatever variation you named your single column in step 2).

9. In the "Choose a column to title your markers" select "Locations" again.

10. You will see your locations positioned on a map!

11. But you will also see a message telling you that some of your rows couldn't be shown and an option to open the data table.

12. Open the data table. Look at the row with the red triangle indicating that they could not be geocoded, and compare them to the geocoded and mapped rows. Ask yourself three questions.
+ First, what happened - invisibly - to the rows that were mapped? What were they matched to? What data has been invisibly added?
+ Second, do these rows have anything in common? Do some of them have something in common? Are some errors? Are some fictional? Are some apparently real places that for some other reason failed to map?
+ Are some of the place names that were coded and mapped probably errors - ie, fictional locations from *Robinson Crusoe* geocoded as small towns in Ohio?

## Think more

Continue to think about the questions in step 10-13, above. Look also at the map above; how does it relate to the MyMaps version you just created? What visions of the world do the two different maps encode? What do they each tell you about *Robinson Crusoe*, and about themselves?

## Write

Write a single paragraph or so in which you succinctly describe the most interesting things you have discovered through this exercise.

No matter what you do, be specific and precise; quote examples; show us that you are worrying away at the texts. Feel free to speculate wildly, but make sure your speculation is hooked to specific observations, readings, interpretations.

## Post

Post your paragraph to Known. Make sure to tag it:  #RobinsonCrusoe #Assignment2 #GoogleMyMaps #Mapping - and another tag or two if you like.

## Extra (not at all required)

For theoretical readings, additional critical approaches,  and tutorials using different mapping technologies see the ["Geospatial Digital Humanities"](http://lkleincourses.lmc.gatech.edu/dh12/schedule/#geo) section of Lauren Klein's Spring 2012 Digital Humanities course at Georgia Tech, Noah Huffman's [Mapping the Broadsides Collection, or, how to make an interactive map in 30 minutes or less](https://blogs.library.duke.edu/bitstreams/2014/05/16/mapping-the-broadsides-collection-or-how-to-make-an-interactive-map-in-30-minutes-or-less/) (a tutorial using Google Fusion Tables to make an interactive map), and the extensive resources in The UCLA Center for Digital Humanities Intro to Digital Humanities class's section on [GIS and Digital Mapping](http://dh101.humanities.ucla.edu/?page_id=244) authored by Elaine Sullivan.

You may also be interested in some histories of cartography, like [these volumes](http://www.press.uchicago.edu/books/HOC/index.html) from the University of Chicago press.

You have eyeballed a comparison between the map printed in *Robinson Crusoe* and the one you created, but the New York Public Library's [Map Warper](http://maps.nypl.org/warper/) lets you digitally align historical maps with contemporary ones. (Only works for some NYPL maps, but an interesting technology to think about.)

----------


Note: This is a new assignment; milage will vary. We would very much like to hear of any problems you have in order to make the next iteration cleaner.

The archival version of our syllabus will be deposited in our Dropbox folder. The most up-to-date copy of our syllabus and exercises will be available on github: https://github.com/rbuurma/rise_2015

This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.
