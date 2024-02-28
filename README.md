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

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig1.jpg)


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

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig2.jpg)

The training data is post-processed with the following filters: 
- Emoticons listed in Table are stripped off 
- Any tweet containing both positive and negative emoticons are removed 
- Retweets are removed
## Dataset Sample
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig3.jpg)

## Text Data Preprocessing
1.	Problems like sentiment analysis are much more sensitive to stop words removal  than document classification. So, none of the stop words should be removed
2.	No need for stemming and lemmatization as all forms of words are covered in GloVe 
3.	URL and USER pattern were removed with URL and USER
4.	Emojis were converted to text
5.	Digits and other special characters were removed
6.	Repeating characters were fixed using regex pattern 
7.	SymSpell spelling correction


## Exploring, Visualizing and Feature engineering of Data

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig4.jpg)


## Exploring, Visualizing and Feature engineering of Data
(Positive wordcloud)
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig5.jpg)

(Negative wordcloud)
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig6.jpg)


## GloVe: Global Vectors for Word Representation
GloVe is an unsupervised learning algorithm for obtaining vector representations for words. Training is performed on aggregated global word-word co-occurrence statistics from a corpus, and the resulting representations showcase interesting linear substructures of the word vector space.
For example, the analogy “king is to queen as man is to woman” should be encoded in the vector space by the vector equation 
king − queen = man − woman. 

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig7.jpg)


##Accuracy of different Models
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig8.jpg)


## Machine Learning model algorithms and accuracy
(Bidirectional LSTM)

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig9.jpg)

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig10.jpg)

## Deployment
Please write a review to score your sentiment for next 72 hours 
https://45862.gradio.app
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig11.jpg)
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig12.jpg)
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig13.jpg)





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

![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig14.jpg)
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig15.jpg)
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig16.jpg)






### Reasons for not removing stop words: ‘only’ is present in nltk stop words
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig17.jpg)
![image](https://github.com/mashukul/data_analytics/blob/main/assets/fig18.jpg)






