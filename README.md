# Project Context
Twitter is a popular microblogging service where users create status messages (called “tweets”).
These tweets sometimes express opinions about different topics. 
Twitter messages have many unique attributes, which differentiates twitter text classification from other classifications
Easy to collect millions of data
The frequency of misspelling and slang much higher
Has a Wide range of Topics
We need a method to automatically extract sentiment (positive or negative) from a tweet. 
Sentiment analysis without manual intervention is very useful because it allows feedback to be aggregated


# Business perspective

Consumers can analyse these sentiments to research products or services before making a purchase. 
Marketers can use this to research public opinion of their company and products, or to analyse customer satisfaction. Organizations can also use this to gather critical feedback about problems in newly released products.

# Business Question?
Can we develop  a model to automatically extract sentiment (positive or negative) from a tweet?

# Models used for Sentiment Analysis

### Conventional modelling techniques:
1. Logistic Regression Classifier
2. Support Vector Machine Classifier

### Approaches:
1. Count Vectors
2. Word Level TF-IDF
3. N-Gram Vectors
4. Char Level Vectors

### With GloVe Pretrained Word vectors:
1. Convolutional neural network
2. Bidirectional LSTM

## Twitter sentiment Classification Flowchart

![image](https://github.com/mashukul/data_analytics/assets/71208684/872ee584-7638-42c3-a9ee-aa58849ba6a9)


# Data Description

1. Data obtained from Kaggle
2. The sentiment140 dataset contains 1,600,000 tweets extracted using the twitter api
3. The tweets have been annotated (0 = negative, 4 = positive) and they can be used to detect sentiment
4. While reviews represent summarized thoughts of authors, these tweets are more casual and limited to 140 characters of text
5. These tweets are not as thoughtfully composed as conventional reviews
6. These tweet messages are mostly based on the following topics
- Company
- Event
- Location
-  Misc.
- Movie
- Person
- Product

## Dataset Post-Processing

![image](https://github.com/mashukul/data_analytics/assets/71208684/93b08f06-a6d0-40fb-9798-37838fa0bd61)

The training data is post-processed with the following filters: 
- Emoticons listed in Table are stripped off 
- Any tweet containing both positive and negative emoticons are removed 
- Retweets are removed
## Dataset Sample
![image](https://github.com/mashukul/data_analytics/assets/71208684/be0bd95d-0dc8-4233-9dd8-b337a3fc775b)

## Text Data Preprocessing
1.	Problems like sentiment analysis are much more sensitive to stop words removal  than document classification. So, none of the stop words should be removed
2.	No need for stemming and lemmatization as all forms of words are covered in GloVe 
3.	URL and USER pattern were removed with URL and USER
4.	Emojis were converted to text
5.	Digits and other special characters were removed
6.	Repeating characters were fixed using regex pattern 
7.	SymSpell spelling correction


## Exploring, Visualizing and Feature engineering of Data

![image](https://github.com/mashukul/data_analytics/assets/71208684/14bbb495-37bb-4a47-8ff4-454339d11bcd)


  

