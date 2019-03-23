# MisInfoText
This repository includes information and resources for automatic misinformation detection, which has become an increasingly important topic in Natural Language Processing and applications for social good. By definition, misinformation refers to the distribution of false information (opposite to facts) in the context of news. In order to automatically detect instances of misinformation, one approach is to combine machine learning and computational linguistic techniques and train predictive models on labeled instances of news articles (fake/real or false/true items). In our attempt, we collect data from a variety of quality sources. In particular, we make sure that the **full text** of each news article and a relaiable **veracity label** indicative of its truth content is provided.

MinInfoText repository consists of three major sections:
* List of datasets that have been published in previous NLP papers and are usefull for building misinformation detection models.
* List of datasets that we have collected by scraping fact-checking websites, whose basic function is to tag false news.
* List of potential fact-checking websites that we have not yet tried in our data collection but could be useful in future work.


 
| __Dataset__ | __Size and type__ | __Labeling system__ | __Notes__ |

allcott2017social | 156 news articles | 5-way (false to true) | Collected from Snopes, Politifact and Buzzfeed fact-checking pages, focused on 2016 US election

ferreira2016emergent | 1,612 news articles | 2-way (false/true) | Unbalanced, originally developed for stance-detection 

rubin2016usingSat | 360 news articles | 2-way (satirical/legitimate) | Balanced by topic and label. A variety of topics. 

