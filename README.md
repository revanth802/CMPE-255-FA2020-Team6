## CMPE-255-FA2020-Team6

# Clustering Based Behavioral and Social Insights w.r.t Pandemic 

### PROJECT TEAM MEMBERS (WITH GITHUB USERNAMES):
- Revanth Krishna Maddula- revanth802
- Harshit Malwiya- harshitmalwiya
- Priyanka Sharma- Priyanka1891
- Kailash Nath Tallapragada- kailashnath979

### Data Source:
The data we will be using is the real-time tweets fetched from Twitter. We will get the tweets using “Tweepy”, an API for twitter-streaming from where we can access the tweets which we import into a pandas data frame. After this, we can perform the required steps to proceed with the project.
We will be focusing mainly on the tweets from the year 2019 and 2020 for this project. The link to the Tweepy API must be done by getting access from the official Twitter developers website specified: https://developer.twitter.com/en

### Description of the problem we are investigating:
The COVID-19 Pandemic has shifted and changed our day to day lives in a very exponential manner. While it is difficult to measure this due to the lack of everyday data of people’s lives, social media can provide us little insight into people’s emotions, spending habits, and actions.

## Preliminary Analysis

### Summary of Data
The data set was generated using the official Twitter API and fetching tweets for the year 2019 and 2020 month-wise. Since Twitter has a well-managed environment for handling and providing data, it provides multiple options to fetch, filter, and collect the data.

### Data Attributes 
- Tweet Id 
- Tweet 
- Created Date
- User Name
- Hashtags
- Location
- Follower Count
- Retweet Count


### Filtering
Dataset was filtered using the following parameters : 
- Start Date
- End Date
- Retweet
- Language

### Data Cleaning
Since Twitter has a fixed format for storing user data and tweets, the dataset was clean of human-induced errors. Tweets have a fixed length of 280 characters. Personal user information is mandatory with built-in validations. 
We performed cleaning as per the following steps : 
- Removed spam tweets
- Removed duplicate tweets
- Removed retweets
- Removed emojis and other graphical data
- Removed HTTP/Https
- Removed any numeric data (if present) in tweets
- Removed any kind of special words
- Verified Users

## Data Visualization:
In the preliminary analysis of the data obtained, we have performed numerous data exploration strategies and have visualized the prevalent trends. 

### Bar Charts: 
One of the most important and interesting features of the data that we have collected is the hashtags used in Twitter posts. We have tried to explore the trends by plotting the bar charts of most used hashtags and the most common words used in tweets in both pre-covid and during the pandemic situation. We have observed that the hashtags #COVID, #coronavirus, #pandemic, etc have been trending since the onset of the pandemic situation.

#### Pre-Covid Common Words Visualization
![BarChart_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/Most_common_words_precovid.png)
#### In-Covid Common Words Visualization
![BarChart_InCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/Most_common_words_covid.png)


### WordCloud: 
We have performed the word cloud visualization on the text obtained from the tweets of Twitter by tokenizing the raw text obtained into words. This visualization is also done for both pre-covid and in-covid periods during the pandemic. We have noticed that the words COVID, Wildfires, Must Protect, Sanitise, etc. have become more and more frequent in the recent past.

#### Pre-Covid WordCloud Visualization
![WordCloud_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/WordCloud_PreCovid.png)
#### In-Covid WordCloud Visualization
![WordCloud_InCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/WordCloud_InCovid.png)


### Violin Charts: 
We have visualized the followers count in pre-covid and during pandemic situations and observed that the followers count declined in the recent past, which could be a potential impact of the pandemic on the people’s day to day lives.

### Word to Vec Embeddings: 
Word embeddings are performed to capture the context of a word in a document, find syntactic and semantic similarity, relation with other words.
Word2vec Technique uses two methods to achieve this, both include Neural Networks :
- CBOW-Model: This model takes an input of context a word as an I/p and tries to predict the word corresponding to the context.
- Skip-Gram Model: This model works in contrast to the CBOW model and takes the input as word and predicts output as context.
In both of the techniques, the network uses back-propagation to learn. CBOW is faster and represents frequent words in a better way, however, Skip-Grams works well with a small dataset and represents rare words effectively. 
#### Pre-Covid Word2vec embeddings
![word2vec_precovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/word2vec_precovid.png)
#### In-Covid Word2vec embeddings
![word2vec_incovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/wordvec_incovid.png)
	
### Methods:

### Vectorization(Feature Extraction): 
- Hashing Vectorizer: The HashingVectorizer applies a hashing function to term frequency counts in each document. The HashingVectorizer has a parameter n_features which is 1048576 by default. When operating hashing, they don't compute dictionary mapping terms to a unique index to use for each one.
- Tfidf Vectorizer: With Tfidfvectorizer we will systematically compute word counts using CountVectorizer and then compute the Inverse Document Frequency (IDF) values and only then compute the Tf-IDF scores. Under the hood, it computes the word counts, IDF values, and Tf-IDF scores all using the same dataset.
- Word2vec vectorizer: Word2vec is a technique for natural language processing. The word2vec algorithm uses a neural network model to learn word associations from a large corpus of text. Once trained, such a model can detect synonymous words or suggest additional words for a partial sentence. Therefore, it is possible to correlate the words in the text by observing the neighboring words.



### Clustering:
K-means: k-means clustering is a method of vector quantization, originally from signal processing, that aims to partition n observations into k clusters in which each observation belongs to the cluster with the nearest mean (cluster centers or cluster centroid), serving as a prototype of the cluster. This results in a partitioning of the data space into Voronoi cells. It is popular for cluster analysis in data mining. k-means clustering minimizes within-cluster variances (squared Euclidean distances).
