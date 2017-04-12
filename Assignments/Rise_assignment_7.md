# Topic Modeling the 1760s (Exercise 7)

+ Check-in on Wednesday, Nov 11, 2015 (try to to have done all of the steps of the assignment including at least one iteration of training topics by then in order to run into bugs, generate questions, etc)
+ Writeup due to Known before class Wednesday, November 18th, 2015
+ Estimated time: 2 hours

### What is topic modeling?

Topic modeling has become popular among humanists seeking to learn about sets of documents (novels, plays, short stories, journals, newspaper articles) too large for a person to read. It uses an algorithm designed to discover what words have a high probability of co-occurring with other words across the entire set of documents. The enabling assumption of topic modeling is that each document is composed out of a percentage of the topics. Of course, this is not in fact the case - the topics are, of course, derived from the documents in a kind of counter-factual reverse-engineering. (More on this in class.)

Crucially, topic modeling doesn’t have any semantic inputs – it doesn’t know ahead of time anything about the meanings of the words it is looking at (in fact, as far as the algorithm understands, it is looking at numbers). You just provide the documents and tell the program how many topics to “train” or create, set a few other parameters, set a stopword list if you like, and the algorithm does the rest.

Once you run the topic modeling program on your set of documents, it gives you some outputs. We will be using MALLET, which will give you a list of groups of words that co-occur (“topics”).  MALLET also gives you a spreadsheet showing what percentage of each topic occurs in each document. It’s then up to us to interpret or label the “topics.”  Some will be fairly obvious. But some of the topics are more ambiguous, and thus in some ways more interesting.

The second output MALLET gives you is a spreadsheet telling you what percentage of each topic occurs in each document. This is also interesting because it might point you to look at chapters (or books, if you are using a large corpus) that you might not otherwise look at. For example, in a model of novels by Richardson split into chapter-length documents, I can tell just from reading what chapters are 75% about a letter-writing topic, but topic modeling might help me notice a series of chapters that are 25% about writing and thus send me to look at them more closely – are those chapters converting language associated with referential representation of writing in some parts of the novel into metaphors? Or are they simply chapters in which letters play a smaller role?

### Preparing Your Corpus

We will be returning to the 1760s in this assignment, so have a quick think back to *Tristram Shandy*.  Our working corpus is comprised of 41 titles printed during the 1760s, in a total of 61 volumes. A little under half are new editions of novels first published in previous decades, such as *Pamela*. Thus, this corpus gives us a sense of the literary field of the 1760s, and a more fleshed-out (though still partial) context for *Tristram Shandy.*

### Topic Modeling 41 Works of Fiction from the 1760s

**NOTE:** If you have any issues downloading or running Topic Modeling Tool, feel free to use any of the 6 iMac workstations in the public computing area in McCabe Library.

These directions have been lightly adapted from Annie Swafford’s excellent [“Topic Modeling assignment”](https://sherlockholmeslondondh.wordpress.com/2015/03/23/topic-modeling-assignment/) for her Digital Tools for the 21st Century: Sherlock Holmes's London class (SUNY New Paltz, Spring 2015).

+ First download [the assignment data](https://github.com/bulbil/rise-assignment7-data/archive/master.zip). This folder also includes the Topic Modeling Tool, a graphical user interface for Mallet. (You can also download the topic modeling tool on its own [here](http://nlp.stanford.edu/software/tmt/tmt-0.4/).)
+ Open the topic modeling tool. If you are on a Mac, there is a good chance that your security settings will refuse to allow you to do such a clearly dangerous thing. To override them, click on the ? you will see on the pop-up box and follow the instructions to locate the downloaded app in finder, press the Control key while clicking the app icon, and choosing Open from the shortcut menu.
+ Click on the button labeled “Select Input File or Dir” and choose the folder with the 1760s corpus that you have saved to your own computer and select “Open.”
+ Click on the button labeled “Select Output Dir.”
+ Click the icon that looks like a folder in the upper right part of the window to create a new folder.
+ Click on the new folder title to rename it.
+ Click “Open.”
+ Under “Number of Topics,” type “50,” under “Number of Iterations,” type “1000,” and under “No. of topic words printing,” type “20.”
+ Click on “Learn Topics.”
+ Once it finishes running, go to your downloads folder and click on the folder you created.
+ Click on output_html, then all_topics to see your results.
+ Click on each topic to see how it’s used.
+ Repeat these steps with different numbers of topics and iterations to explore how this affects your results.  Give the output folder a new, descriptive name each time. Also experiment with checking and unchecking “Remove Stopwords” to see what happens.

### Write

For this response, we will focus on looking at and labeling the topics, but you are also free to think further about the output showing you topics in documents. To begin thinking, choose ten interesting topics, list them, and label them. (Remember to include a note on the settings you used to generate those particular topics. Include the number of iterations, number of topic words, and number of total topics trained.)

Then write just a few paragraphs, thinking about some of the following questions:

Do the topics remind you of anything that arose for us around Tristram Shandy? Can you trace any of the lineaments of TS in this 1760s corpus via your examination of the topics you generated?  Can you connect any of the topics you have labeled to bigger arguments about the novel by Watt, McKeon, Armstrong, Habermas, Anderson, or Barthes?

Also possibly of interest: is there any apparent relation between what Barthes is arguing in “The Reality Effect” and what we are doing when we topic model 1760s novels? Specifically, you may notice that topic modeling’s treatment of documents as “bags of words” and the way we tend to prefer nouns when we apply a stoplist (sometimes - we will discuss the stopword process more in class) almost makes the novel seem like ALL reality effect. Thoughts about this?

### Further optional reading

["Topic Modeling and Digital Humanities"](http://journalofdigitalhumanities.org/2-1/topic-modeling-and-digital-humanities-by-david-m-blei/) by David Blei in the special topic modeling issue of the Journal of Digital Humanities offers an accessible introduction.

In the same issue, Megan Brett’s ["Topic Modeling: A Basic Introduction"](http://journalofdigitalhumanities.org/2-1/topic-modeling-a-basic-introduction-by-megan-r-brett/) reinforces the overview and the “applications” essays by Lisa Rhody and others give some use cases.

After doing this to orient yourself, you may wish to read Ted Underwood’s more technical blog post ["Topic modeling made just simple enough"](https://tedunderwood.com/2012/04/07/topic-modeling-made-just-simple-enough/) for a more detailed perspective.

For more technical detail, David Mimno's video ["The Details: Training and Validating Big Models on Big Data"](http://journalofdigitalhumanities.org/2-1/the-details-by-david-mimno/) may be useful (without understanding all of it, I find it helpful).

Scott Weingart’s 2012 [Topic Modeling for Humanists: A Guided Tour](http://www.scottbot.net/HIAL/?p=19113) is partly his own explanation and partly a nice overview of increasingly complex introductions to topic modeling; it is a bit outdated at this point, however, as it won’t include work published after 2012.

### Acknowledgements

This assignment was produced in collaboration with Nabil Kashyap (Swarthmore Librarian for Digital Initiatives and Scholarship)  and Lindsay Van Tine (Penn-Swarthmore CLIR Fellow).

It draws heavily on Annie Swafford’s [“Topic Modeling assignment”](https://sherlockholmeslondondh.wordpress.com/2015/03/23/topic-modeling-assignment/) for her Digital Tools for the 21st Century: Sherlock Holmes's London class (SUNY New Paltz, Spring 2015).
