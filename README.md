# PersonaBank - A Corpus of Story Intention Graphs. 

Version: Version 1.0. Updated May 17, 2016.

## Overview 
We present a new corpus, PersonaBank, consisting of 108 personal stories from weblogs that have been annotated with their Story Intention Graphs, a deep representation of the fabula of a story. We describe the topics of the stories and the basis of the Story Intention Graph representation, as well as the process of annotating the stories to produce the Story Intention Graphs and the challenges of adapting the tool to this new personal narrative domain. We also discuss how the corpus can be used in applications that retell the story using different styles of tellings, co-tellings, or as a content planner.

## The Data
- 108 blog stories (in original/)
- Their corresponding .VGL (in vgl/) and Scheherazade realization files (in sch/)
- Tutorial for blog annotation in Scheherazade (annotationTutorialForBlogs.pdf)
- Spreadsheet describing the stories, their topics, polarity, and an excerpt of the story (personaBank.csv)
- Spreadsheet describing the topic distribution (topics.csv)

## Notes
1. Download Scheherazade annotation software at: http://www1.cs.columbia.edu/~delson/software.shtml

2. The original Scheherazade tutorial is available at: https://sites.google.com/site/scheherazadetutorial/

3. Due to the nature of the Scheherazade annotation, names have been anonymized so that a name like Brian will become Jake# with trailing '#'. These '#' are only in the original story files. A .vgl loaded into Scheherazade and the Scheherazade text file will look like 'Jake' without the trailing '#'.

4. Format of personaBank.csv. The header is: 
```
UniqueId,Suffix,FileName,polarity,Interp layer,Topic(s),First few words
```

Interp layer indicates if this story has been annotation in the interpretation layer. Polarity indicates the overall polarity of the story.

5. Format of topics.csv. The header is:
```
topic,parentTopic,total,posCount,posIds,negCount,negIds
```

If the parentTopic = -1, this is a main topic. For example:
```
health,-1,16,1,[108],15,[31,105,2,38,105,44,24,29,106,15,17,21,106,102]
```

Otherwise, it is a subtopic:
```
life,health,2,1,[108],1,[31]
```

The posIds and negIds correspond to the Uniqueid in personaBank.csv

## Citation
If you use this data in your research, please refer to and cite: Lukin, Stephanie M., Bowden, Kevin, Barackman, Casey, Walker, Marilyn A. ["A Corpus of Personal Narratives and Their Story Intention Graphs"](http://lrec.elra.info/proceedings/lrec2016/pdf/356_Paper.pdf). In Proceedings of the 10th International Conference on Language Resources and Evaluation (LREC), Portorož, Slovenia, 2016.

## Related Works
- Elson, David K. ["DramaBank: Annotating Agency in Narrative Discourse."](http://lrec.elra.info/proceedings/lrec2012/pdf/866_Paper.pdf) In Proceedings of the 8th International Conference on Language Resources and Evaluation (LREC), Istanbul, Turkey, 2012.
- Download Scheherazade GUI to view and edit SIGs: http://www1.cs.columbia.edu/~delson/software.shtml

## Works that use this corpus:
- Lukin, Stephanie M., Walker, Marilyn A. ["Generating Sentence Planning Variations for Story Telling."](https://aclanthology.org/W15-4627.pdf) In The 16th Annual SIGdial Meeting on Discourse and Dialogue (SIGDIAL), Prague, Czech Republic, 2015.
- Lukin, Stephanie M., Walker, Marilyn A. ["Narrative Variations in a Virtual Storyteller."](http://link.springer.com/chapter/10.1007/978-3-319-21996-7_34) In The 15th International Conference on Intelligent Virtual Agents (IVA), Delft, The Netherlands, 2015.
- Rishes, Elena, Lukin Stephanie M., Elson, David K., Walker, Marilyn A. ["Generating Different Story Tellings from Semantic Representations of Narrative."](https://www.researchgate.net/profile/Marilyn-Walker-5/publication/280297613_Narrative_Variations_in_a_Virtual_Storyteller/links/55aff92a08aeb0ab46698352/Narrative-Variations-in-a-Virtual-Storyteller.pdf) In International Conference on Interactive Digital Storytelling (ICIDS), Istanbul, Turkey, 2013.





