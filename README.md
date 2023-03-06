# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) 




# Project 3: Standardized Test Analysis


---
## Problem Statement

During a recent expedition to the ruins of alpha-Earth, an exploration team recovered a semi-operable server containing data from the popular 21st century website Reddit, with intact data from two notable subreddits: r/anime and r/Naruto.  

Additionally, the team discovered a manual on early 21st century data science techniques for classification and machine learning.  These data remnants were transmitted to my team at the Neo-Earth Research Council for further study.  

Combining the wisdom of these two cultural artifacts, we use these 21st century methods to analyze this 21st century data.  Fascinating, no?  We explored the use of natural language processing and several classification algorithms to differentiate between posts from r/anime vs. those from r/Naruto.  

We present these findings at the 3023 Mars Conference on Pre World War 3 Humanoid Anthropology.  

---
## Executive Summary

The Random Forest (with unlimited depth, single-word n-grams only, and without using stop words) narrowly outperformed its competitors with an accuracy of 88.03%.

|Rank|Algorithm|Accuracy|
|---|---|---|
|1|Random Forest|88.03%|
|2|TfidfVectorizer|87.12%|
|3|Naive Bayes|86.28%|
|4|K Nearest Neighbors|75.19%|

# ![](https://git.generalassemb.ly/wangdj3/project-3/blob/master/assets/RandomForest_ConfusionMatrix.png) 

Top 15 Most Common Words in Combined Sample:

|Rank|Word|Count|
|---|---|---|
|1|https|5497|
|2|anime|4320|
|3|naruto|2544|
|4|like|1784|
|5|episode|1710|
|6|com|1681|
|7|redd|1490|
|8|link|1470|
|9|just|1457|
|10|youpoll|1352|
|11|amp|1226|
|12|sasuke|945|
|13|know|917|
|14|think|905|
|15|watch|791|


---
## Data Background

Our data was scraped from reddit using the Pushshift Reddit API.[1]  5,000 submissions were scraped from both r/anime and r/Naruto subreddits, after which duplicates were removed.

---
## Primary Findings

- While all classification algorithms tested outperformed the baseline (50.8%) significantly.  

- The Random Forest had the highest prediction accuracy (88.03%).  

- The K Nearest Neighbors method performed worst out of the algorithms evaluated



### Ranking of Classification Algorithms used:

|Rank|Algorithm|Accuracy|
|---|---|---|
|1|Random Forest|88.03%|
|2|TfidfVectorizer|87.12%|
|3|Naive Bayes|86.28%8|
|4|K Nearest Neighbors|75.19%|

---
## Comments/Instructions for Graders

- Initial data grab via API is performed in 'my-project3-getdata.ipynb'

- Datasets are then processed in 'my-project3-data-cleaning.ipynb'

- Cleaned datasets are merged and classified in 'my-project3-classification.ipynb'


---
## Sources & References

1.  [`Pushshift Reddit API`](https://github.com/pushshift/api) 