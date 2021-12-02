# Stock-Prediction

If you are here at this repo this means that either you are interested in stock market or in Data science. I perticularly was interested in both. In this repo you have the necessary data and code to do Price prediction of Apple stocks, or any other company provided that you have twitter data related to that company.

---
**NOTE**
Note : This repo is for studying purposes only and is still in developing phase, you are not advised to gamble on this algorithm alone.
--
## INTRODUCTION 

Stock market prediction has been a hot topic of study. Stock market prices are mostly driven by fresh information and follow a random walk pattern. Several people have attempted to extract patterns in the way stock markets operate and respond to external stimuli, despite the fact that this theory is largely acknowledged by the scientific community as a basic paradigm regulating markets in general.
In this project, we tested a hypothesis based on the assumption that people's emotions and moods influence their decision-making process, resulting in a direct association between "public sentiment" and "market sentiment". We use publicly available Twitter data to do sentiment analysis to determine the public mood and classify them (classification of tweets with the sentiment) i.e. positive/ negative/ neutral.

## DATASET

The project is divided into 2 major components,
Dealing with twitter data and finding out the twitter sentiment. The format of the dataset is as follows:
For training, an IEEE dataset of labelled tweets is used which has 5000 labelled tweets and ~100k unlabelled tweets. For testing, date wise tweets starting from 2014-1-1 to 2015-12-31. Each file has a json-like structure. 
Fig Showing word-cloud generated of the IEEE stock market tweet dataset(CSV file provided).
For live streaming, we have used tweepy api to call tweets but it so turns out that the live streaming tweets are only allowed for 7 days which leaves us 5 days for final prediction for final analysis.

For dealing with historical data of stocks, yahoo finance api is used. We downloaded the stocks data from the API, where the dataset contains 7 columns which retrieves the data from the given start date to end date to which we want to retrieve the data. The stocks data can be retrieved from the api,  upon the timely intervals we need. Later, this data is used for training the final model using the twitter sentiment analysis. We used the sentiment class and score as features with the open and close values of the stock and lagged the data 

## ALGORITHM

In our project we have used a Logistic Regression algorithm to build the model. It can predict the probability of occurrence of an event by fitting data to a logit function. Log-linear classifier works by extracting some set of weighted features from the input, taking logs, and combining them linearly. Before applying the logistic regression on the tweets we have calculated the TF, IDF of tweets and keeping them as features we are applying Logistic regression. 
The significant phrases used in TF-IDF are:

- TF = (the count of the term t appears in a text document)/(Number of terms in the document).
- IDF = log(D/d), where, D is the number of documents and the number of documents a term t has appeared is referred to as d. 
- TF IDF = TF*IDF

## RESULTS
