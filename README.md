# MisInfoText
This repository includes information and resources for automatic misinformation detection, which has become an increasingly important topic in Natural Language Processing. By definition, misinformation refers to the distribution of false information (opposite to facts) in the context of news. In order to automatically detect instances of misinformation, one approach is to combine machine learning and computational linguistic techniques to build predictive models on labeled instances of news articles (fake/real or false/true items). Such models could then be applied to an unseen news article and score its veracity with respect to its linguistic characteristics. At the [Discourse Processing Lab](http://www.sfu.ca/discourse-lab/software_and_data/demo.html), we have started a project to collect data suitable for automatic misinformation detection from a variety of quality sources. In particular, we make sure that the **full text** of each news article and a reliable **veracity label** indicative of its truth content is provided in our data collections.

MinInfoText repository consists of three major sections:
* List of datasets that we have collected by scraping fact-checking websites, whose basic function is to find and tag suspicious news.
* List of other datasets that have been published in previous NLP papers and are useful for building misinformation detection models.
* List of potential fact-checking websites that we have not yet used in our data collection effort but could be employed in future work.


## Data scraped from fact-checking websites

We are developing a large dataset containing instances of fact-checked news articles. In order to do so, we make use of automatic scrapers to crawl fact-checking websites for false/true claims and headlines, links to the original news articles spreading them and the veracity labels given by the fact-checkers. Details of this process depend on the specific structure of the fact-checking website and the amount of information they include about the sources of a discussed piece of news. Currently, we have scraped and cleaned data from four fact-checking websites (snopes, buzzfeed, politifact and emergent).

We have published three large datasets through [our lab website](http://fakenews.research.sfu.ca/), which still require manual verification of the alignment between the claims and the original news texts (both available in our data tables). Our annotators have manually verified this alignment for a relatively small portion of the data (Snopes312, BuzzfeedUSE and BuzzfeedTop collections) and published the resulting dataset through [another github repository](https://github.com/sfu-discourse-lab/Misinformation_detection).

Please refer to the following papers for details on the data collection process and our automatic misinformation detection experiments:


* Fatemeh Torabi Asr, Mehrdad Mokhtari and Maite Taboada, to appear. ["Misinformation detection in news text: automatic methods and data limitations"](https://www.sfu.ca/~mtaboada/docs/publications/Asr_Mokhtari_Taboada.pdf). In Maci, S., M. Demata, M. McGlashan and P. Seargeant (eds.) [The Routledge Handbook of Discourse and Disinformation](https://www.routledge.com/The-Routledge-Handbook-of-Discourse-and-Disinformation/Maci-Demata-McGlashan-Seargeant/p/book/9781032124254). to appear.

* Fatemeh Torabi Asr and Maite Taboada, 2018. ["The Data Challenge in Misinformation Detection: Source Reputation vs. Content Veracity"](http://aclweb.org/anthology/W18-5502). In Proceedings of The First Workshop on Fact Extraction and Verification, EMNLP 2018.

* Fatemeh Torabi Asr and Maite Taboada, 2019. "Big Data and Quality Data for Fake News and Misinformation Detection". Journal of Big Data and Society.

We will soon publish a larger dataset that we have verified by recruiting annotators on the [Figure Eight platform](https://www.figure-eight.com/). So please keep in touch for more to come!

We also welcome suggestions for inclusion of other datasets in our list. Please see what follows and let us know if you think your dataset can be listed too!



## List of veracity-labeled text collections

| __Data paper__ | __Size and type__ | __Labeling system__ | __Notes__ |

[Nielsen D and McConville R (2022)](https://mumin-dataset.github.io/) | 12,914 claims, 21,565,018 tweets, 1,986,354 users, 10,920 articles, 6,573 images | 2-way (misinformation and factual) | Collected from 115 different fact-checking organisations in 41 different languages. Features dozens of different events and topics.

Allcott H and Gentzkow M (2017) | 156 news articles | 5-way (false to true) | Collected from Snopes, Politifact and Buzzfeed fact-checking pages, focused on 2016 US election

Ferreira W and Vlachos A (2016) | 1,612 news articles | 2-way (false/true) | Collected from Emergent.org, unbalanced, originally developed for stance-detection

Rubin VL, Conroy NJ, Chen Y and Cornwell S (2016) | 360 news articles | 2-way (satirical/legitimate) | Balanced by topic and label. A variety of topics.

Zhang  AX,  Ranganathan  A,  Metz  SE,  et al. (2018) | 40 news articles | Multiple (credibility indicators) | Continuous effort with the future goal of annotating 10,000 articles.

Perez-Rosas   V,   Kleinberg   B,   Lefevre   A   and   Mihalcea   R (2017) | 480 news articles | 2-way (fake/legitimate) | Balanced by topic and label. Fake items were artificially generated by Turkers.

Perez-Rosas   V,   Kleinberg   B,   Lefevre   A   and   Mihalcea   R (2017) | 200 news articles | 2-way (fake/legitimate) | Balanced by topic and label. Focused on celebrity stories.

Wang WY (2017)  | 12.8K short statements | 6-way (false to true) | Collected using the Politifact API.

Thorne   J,   Vlachos   A,   Christodoulopoulos   C   and   Mittal   A (2018)  | 185K short statements and supporting/refuting Wikipedia documents | 2-way (original/mutated) | Originally developed for stance-detection. Mutated claims were artificially generated.

[Asr FT, Taboada M (2019)](https://github.com/sfu-discourse-lab/Misinformation_detection/blob/master/buzzfeed-v02-originalLabels.txt.zip) | 1,380 news articles | 4-way (false, true, mixture, no factual content) | Collected using a pivot Buzzfeed dataset. Focused on the US election topic.

[Asr FT, Taboada M (2019)](https://github.com/sfu-discourse-lab/Misinformation_detection/blob/master/buzzfeed-top.csv.zip) | 33 news articles | 4-way (false, true, mixture, no factual content) | Collected using a pivot Buzzfeed dataset. A variety of topics.

[Asr FT, Taboada M (2019)](https://github.com/sfu-discourse-lab/Misinformation_detection/blob/master/snopes_checked_v02.csv.zip) | 312 news articles | 5-way (false to true) | Collected from Snopes. Balanced by label. A variety of topics. Includes stance information (articles for or against a labeled claim).


## List of potential fact-checking websites

We have investigated the following sources in our search for the fact-checking websites that can be pivoted in automatic data collection. The items marked by star are either currently under scraping at our lab or may be considered in the future. Our source to find verified fact-checkers in the first place is [poynter](https://ifcncodeofprinciples.poynter.org/signatories).

| __Website__ | __Notes on automatic scraping possibility__ |

* BOOM - poor format to extract data from, labels not present almost all of the time
* Check Your Fact* - there looks to be a pattern and data extracting could work, clear format
* Factcheck.org* - good format in the debunking fact section
* Ferret Fact Service* - data extraction may work, labels (mfalse, false, true, mtrue, halftrue)
* Full Fact - little labels but may be able to conclude with the paragraph on the side
* Lead Stories - no pattern suitable for automatic data extraction
* Pesa Check* - clear labels, clear format and pattern, may be able to extract
* PolitiFact* - currently using
* Rappler - no labels, would be extremely difficult to extract
* RMIT ABC Fact Check - many different labels all over the place, very hard to generalize
* Snopes* - currently using
* South Asia Check - no labels, format unclear
* The Conversation FactCheck - formal unclear, pattern very inconsistent
* TheJournal.ie Fact Check* - clear pattern and labels, possibility for data extraction
* The Washington Post Fact Checker* - labels, clear pattern, possibility for data extraction
* VoxCheck - very in depth analysis, few labels, not necessarily news stories but long term coverage of an event, will be very difficult to extract data
* AP Fact Check - no labels, no apparent pattern
* Climate Feedback* - very clear pattern, format and sources; however, a variety of labels
* FactCheck Northern Ireland - no labels, format or pattern



