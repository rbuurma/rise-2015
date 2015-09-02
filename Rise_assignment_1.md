# People, Places, Time, Money: Listing *Robinson Crusoe*

Next week we will see that in *The Rise of the Novel*, Ian Watt argues that, like the jury in a court of law, the readers of a novel expect

>to know 'all the particulars' of a given case - the _time_ and _place_ of the occurrence; both must be satisfied as to the _identities_ of the parties concerned, and will refuse to accept evidence about anyone called Sir Toby Belch or Mr. Badman -- still less about a Chloe who has no surname and is 'common as the air'...". (31, emphasis added)

Though we may quarrel with many of Watt's implicit and explicit claims (including the confidence with which he refers to a thing called a "novel"),  our reading of *Robinson Crusoe* so far has likely convinced us that specific times, places, and names - as well as amounts of money and dates -- seem important to this novel at least, though we will differ as to our interpretation of precisely *how* they are important.

This exercise helps us extend our thinking about the fictional representation of places, characters' names, times and dates, and money and by using a tool called the [Stanford Named Entity Recognizer](http://nlp.stanford.edu/software/CRF-NER.shtml) to extract references to time, location, organization, person, money, percent, and date from the text of *Robinson Crusoe*.  In short, we are going to reduce the amazingly weird and complex *Robinson Crusoe* to a list,  extracting just some data in order to create a deliberately impoverished representation of RC - one that leaves out most of the novel to let us look more closely and comprehensively at a very specific part of it.

After extracting creating these lists, we will try our hand at interpreting them. How is reading these lists different from or similar to reading *Robinson Crusoe* in a more continuous way, from beginning to end or cover to cover?

We also want to think about the lists of food, animals, tools, physical characteristics, and events we have already found IN *Robinson Crusoe* - what is their function?  Moving from literary criticism to named entity extraction and text manipulation and and back to literary criticism should open up this question further.

In short, in this assignment we will

1. Use the Stanford NER to classify some of the words in *Robinson Crusoe* as Time, Location, Organization, Person, Money, Percent, or Date
2. Convert the NER output into into seven separate lists
3. Do some close reading of and thinking about one or more of those lists

(Note for the curious: Next week, we will build on this work by using some additional tools and techniques to help us visualize some of the data to help us interpret it in new ways - and you are welcome to begin doing this right away by yourself if you have the time and inclination. Right now, however, for the sake of this assignment we are sticking with plain old lists.)

Here are very detailed, step-by-step instructions. If you prefer, you are free to skip the instructions, try to figure out  how to do it yourself, and skip to the last two sections.

##Using the Stanford NER on *Robinson Crusoe*

1. Follow the directions to install the [Stanford Named Entity Recognizer](http://nlp.stanford.edu/software/CRF-NER.shtml) on your computer.

2. Open the file named ner-gui.command.

3. This will open the NER program in two windows: in your Terminal and in a Java application window. In the second window, erase the pre-loaded text and use the Open File command to open the clean Project Gutenberg version of *Crusoe* you will find in both the assignment folder and the repository. (We will talk more about how we create and find usable machine-readable text files of our novels in future assignments, and you will learn to create them yourself.)

4. Click "Classifier" and choose "Load CRF from file." Navigate to where you have installed the NER and find the "Classifiers" folder. Select the file with 7 entities that ends in gz. The seven entities will appear on the right side of the window.

5. Click the "Run NER" button. It will probably take a while to run.

6. Eventually, the text of RC will appear in the window with the relevant words tagged in the various entity colors. Interesting! But not very easy to use.

7. Luckily, a more flexible form of the tagged entities awaits you in your Terminal. Click over to the Terminal now, and use Command-A and then Command-C to copy the entire list.

8. Open [Textwrangler](http://www.barebones.com/products/textwrangler/) - or download it and open it if you don't already have it installed. Create a new file,  paste the full list into it, and name it in some regular, identifiable way (for example, RCNER.txt or RCList.txt).

If you get stuck, refer to the very complete instructions in Michelle Moravic's [How to Use the Stanford NER and Get Results](http://historyinthecity.blogspot.com/2014/06/how-to-use-stanfords-ner-and-extract.html) or ["Using the Stanford Named Entity Recognizer to extract data from texts"](http://themacroscope.org/wp-content/uploads/2014/09/textanalysisandviz.html) in the preprint version of *The Historian's Macroscope*.

If you are still stuck, ask a classmate who has done the exercise successfully or contact Nabil Kashyap (nkashya1 at swarthmore dot edu) or me. If  you have trouble and you are on a Mac, check to see if you have the most recent version of the [Java Development Kit](<http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html>) installed.  If you are on a PC, things are going to be a bit trickier. If you don't have access to a Mac, either consult the relevant section of ["Using the Stanford Named Entity Recognizer to extract data from texts"](http://themacroscope.org/wp-content/uploads/2014/09/textanalysisandviz.html) in the preprint version of *The Historian's Macroscope* or contact us for help or both. (I hope to update this assignment to include complete PC instructions shortly.)

## Manipulate and Clean Your Data

Great, you have a long list of  tagged terms.  Now you want to make seven separate lists. This will not take long.

1. Open the NER output file you want to work with in TextWrangler or equivalent text editor.

2. Select the file in the lefthand text tab. Under the "Text" menu, select "Process Lines Containing" and enter PERSON. Make sure you check box for "copy to new document." Click "Process".

3. You should now have a new file containing only the "PERSON" lines. Save it with an easily legible, regular name (like RCNER_persons.txt). Now scroll through, taking a look at the names. What did you expect? What do you see? What are you learning already?

4. You will see that there are many duplicates, and also perhaps some errors - errors that may be generated by either bad input data (misspellings or mis-transcriptions in the Project Gutenberg file, for example) or errors generated by the NER (places misrecognized as names, for example). Right now we don't need to worry about errors - but if you see some that occur regularly you might want to think about why this happened.

5. To de-duplicate in order to create a list with only one instance of every occurrence, under the "Text" menu, select "Process Duplicate Lines." Make sure "Leaving one" and "Unique Lines to New Document" are checked. Save your new document with a legible, regular name.

Take a look at the new document; think about its length as compared to the length of the original document. What does this tell you?

In another sense, we could say that though we have removed the literal duplicates, in another sense "duplicates" remain in the form of multiple different words or phrases referring to the same character or place, for example. What can you learn about the language and logic of *Robinson Crusoe* from these?

Extra: Depending on what else you might want to do with your data in the future, you may want to clean or manipulate it in other ways. For more sophisticated comparison between , save one or more of your lists with a .csv instead of a .txt ending, download [OpenRefine](http://openrefine.org/) and watch the short introductory videos to learn how you can quickly count occurrences, identify and condense similar names, etc.

As always, remember to create a new, clearly and regularly-labeled copy of your data every time you work with it in a new way.


Repeat for the six other types of extracted entities.

## Read and Think

So now you have extracted seven lists from your novel. Starting with two questions at the back of your mind - What can we learn from these lists about *Robinson Crusoe*? What can we learn from *Robinson Crusoe* about lists? -  slowly read one or more of your lists.

In a basic sense - did the NER work? In the case of any given list, did it work as you expected? Which of your assumptions about *Robinson Crusoe* are reinforced by your reading of the list(s)? Which assumptions or readings were challenged or denaturalized?

## Write

Write a single paragraph or so in which you succinctly describe the most interesting things you have discovered through your work and thought -  and perhaps speculate on questions your work with these lists has opened up and how you might answer them. You can do this however you like. Suggestions to get you started: You might return to a passage from the novel and reading it alongside a list or an aspect of a list; you might compare one of your lists to a literal list from RC; you might speculate on how one of these lists helps you reread some aspect of RC, or confirms or challenges some aspect of your thinking about the novel.  You might simply spend some time unwinding your reading of one of the lists. You might spend a paragraph interpreting a comparison of an original and a de-duplicated list.

No matter what you do, be specific and precise; quote examples; show us that you are worrying away at the texts. Feel free to speculate wildly, but make sure your speculation is hooked to specific observations, readings, interpretations.

## Post

Post your paragraph to Known. Make sure to tag it:  #RobinsonCrusoe #Assignment1 #NER - and another tag or two if you like.

## Extra (not at all required)

What is a list? What kind of form is it? How do lists work in *Robinson Crusoe*? Is there a history of the list? Can you find an academic history of the list? A popular history of the list? How many lists have you encountered today? Ordered or unordered, digital or analog, short or long?

What kind of order do the lists we created have? How might that order have meaning? Or what would we need to know or do to access that meaning?

How does the Stanford NER work? Do a bit of research and write a quick explanatory post.

In ["Mapping Mutable Genres"](http://arxiv.org/abs/1309.3323), Ted Underwood, Loretta Auvil, and Boris Capitanu discover a correlation between "first-person" narration, travel, and quantification.

>first-person pronouns are positively correlated with terms that describe travel—and especially travel by sea. We found one clue to this association when we looked at a list of titles sorted by our classifier. A remarkable number of the works recognized as most strongly “first-person” in character belonged to the genre of the Robinsonade. We were aware that *Robinson Crusoe* (1719) was a widely-reprinted and frequently-imitated novel, but we hadn’t realized just how long and vigorously this tradition endured. *The Swiss Family Robinson* (1812) was joined by an *English Family Robinson* (1852), for instance, and eventually by a *Robinson Crusoe of the Nineteenth Century* (1884), and many others. The castaway premise obviously encourages a story to rely on first-person narration, and we suspect it may also encourage quantification. Crusoe’s obsession with enumeration and accumulation is famously part of the colonial logic of his narrative, which transforms (ostensibly) uninhabited land into a well-governed productive system. ("Mapping Mutable Genres," Section 2C)

They hypothesize that the reason may be that the castaway premise, or "the combination of a first-person narrator, a colonial setting,
and acquisitive quantification" in adventure fiction may encourage both first-person narration and quantification. Based on your work examining the NER outputs of Time, Money, Percent, and Date, can you offer any hypotheses of your own based just on *Robinson Crusoe*? If you wanted to extend what you've learned from the NER data about languages of quantification in RC, what further information would you need? What other correlations within RC might you look for? If you wanted to extend your investigation outward to the Robinsonade, or to adventure or travel fiction more broadly, how might you go about doing that?

What else?

----------

This assignment is indebted to Michelle Moravic's [How to Use the Stanford NER and Get Results](http://historyinthecity.blogspot.com/2014/06/how-to-use-stanfords-ner-and-extract.html) and ["Using the Stanford Named Entity Recognizer to extract data from texts"](http://themacroscope.org/wp-content/uploads/2014/09/textanalysisandviz.html) in *The Historian's Macroscope*.  I was also inspired by Scott Enderle's thinking about the value of lists in his ["Against Visualization"](https://readingfromadistance.wordpress.com/2015/04/18/against-visualization/) post at Skidmore's [Reading From A Distance](https://readingfromadistance.wordpress.com/). And a huge thanks to Nabil Kashyap for tireless testing and invaluable suggestions.

Note: This is a new assignment; milage will vary. We would very much like to hear of any problems you have in order to make the next iteration cleaner. In addition, this version of the assignment assumes root privileges on a fairly recent version of OSX, but we aspire for the next draft to include instructions for a wider variety of platforms.

The archival version of our syllabus will be deposited in our Dropbox folder. The most up-to-date copy of our syllabus and exercises will be available on github: https://github.com/rbuurma/rise_2015

This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/ or send a letter to Creative Commons, 444 Castro Street, Suite 900, Mountain View, California, 94041, USA.
