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


## Exploring, Visualizing and Feature engineering of Data
(Positive wordcloud)
![image](https://github.com/mashukul/data_analytics/assets/71208684/fc374304-a89e-4179-a67b-c28e1286b740)

(Negative wordcloud)
![image](https://github.com/mashukul/data_analytics/assets/71208684/529433fc-0c8e-45af-b1d6-f9d89f414a37)


## GloVe: Global Vectors for Word Representation
GloVe is an unsupervised learning algorithm for obtaining vector representations for words. Training is performed on aggregated global word-word co-occurrence statistics from a corpus, and the resulting representations showcase interesting linear substructures of the word vector space.
For example, the analogy “king is to queen as man is to woman” should be encoded in the vector space by the vector equation 
king − queen = man − woman. 
![image](https://github.com/mashukul/data_analytics/assets/71208684/75972499-0314-4273-a46b-563403bdc4bf)


##Accuracy of different Models
![image](https://github.com/mashukul/data_analytics/assets/71208684/19a94f01-c979-4a4e-bd48-790229c212b0)


## Machine Learning model algorithms and accuracy
(Bidirectional LSTM)

![image](https://github.com/mashukul/data_analytics/assets/71208684/3630b625-256c-4fd3-9f9f-27ea15811f68)

![image](https://github.com/mashukul/data_analytics/assets/71208684/6bddf01a-b142-441e-8064-71b08d04596b)

## Deployment
Please write a review to score your sentiment for next 72 hours 
https://45862.gradio.app
![image](https://github.com/mashukul/data_analytics/assets/71208684/bdb422ff-e123-45c9-b8fe-783fe7539224)
![image](https://github.com/mashukul/data_analytics/assets/71208684/7b3cc3ad-7c48-4739-b9be-557af3132a80)
![image](https://github.com/mashukul/data_analytics/assets/71208684/17b3a08d-c5b1-44ce-82b5-2526b694abd7)





## Summary
1.	We have built a model for classifying tweeter message to negative and positive without any manual intervention
2.	Pre-processing in sentiment analysis text classification is different from document or theme classification.
3.	Convolutional Neural network also give better result for text classification.
4.	At first SVM and LR classifier are used 
5.	Most advanced RNN for text classification (Bidirectional LSTM) along with pretrained word representation GloVe outperforms all conventional models 
6.	Our final model has an accuracy of 83.04

## Future scope

1.	If we have a dataset which labelled with different categories like company, product, service model could be used to analyze sentiment for the respective fields.
2.	Then the training the model will be easy and predictions will be more targeted
3.	This model can also be used for pre-election public sentiments.
## Reference
1.	Dataset link: https://www.kaggle.com/datasets/kazanova/sentiment140
2.	Citation: Go, A., Bhayani, R. and Huang, L., 2009. Twitter sentiment classification using distant supervision. CS224N Project Report, Stanford, 1(2009), p.12.
3.	https://medium.com/@limavallantin/why-is-removing-stop-words-not-always-a-good-idea-c8d35bd77214

## Appendix
### Reasons for not removing stop words: ‘Not’, ‘but’ are present in nltk stop words

![image](https://github.com/mashukul/data_analytics/assets/71208684/547c748d-2e7d-4767-9a98-1e51e09a227d)
![image](https://github.com/mashukul/data_analytics/assets/71208684/e3aaf8e3-cf91-4115-a40f-a3d04460cbef)
![image](https://github.com/mashukul/data_analytics/assets/71208684/ddd69732-3442-4807-9c4b-7bef012ef11a)




### Reasons for not removing stop words: ‘only’ is present in nltk stop words
![image](https://github.com/mashukul/data_analytics/assets/71208684/5754bcaa-3dac-4dad-b161-1ea4f721cff3)
![image](https://github.com/mashukul/data_analytics/assets/71208684/4bc1235a-465e-43c2-90d9-7a25d794c1ce)






