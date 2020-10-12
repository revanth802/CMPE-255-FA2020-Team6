# CMPE-255-FA2020-Team 6

## PROJECT PROPOSAL:

### PROJECT TEAM MEMBERS (WITH GITHUB USERNAMES):
- Revanth Krishna Maddula- revanth802
- Harshit Malwiya- harshitmalwiya
- Priyanka Sharma- Priyanka1891
- Kailash Nath Tallapragada- kailashnath979

### 1. Project Title: 
Clustering Based Behavioral and Social Insights w.r.t Pandemic 

### 2. Data Source:
The data we will be using is the real-time tweets fetched from Twitter. We will get the tweets using “Tweepy”, an API for twitter-streaming from where we can access the tweets which we import into a pandas data frame. After this, we can perform the required steps to proceed with the project.
We will be focusing mainly on the tweets from the year 2019 and 2020 for this project. The link to the Tweepy API must be done by getting access from the official twitter developers website specified: https://developer.twitter.com/en

### 3.Description of the problem we will investigate:
The COVID-19 Pandemic has shifted and changed our day to day lives in a very exponential manner. While it is difficult to measure this due to lack of everyday data of people’s lives, social media can provide us little insight into people’s emotions, spending habits, and actions.
Tweets can be broadly categorized in the following topics : 
- Activities
- Product Reviews
- Emotions
- Opinions about Social Topics

By analyzing tweets over the pre-COVID and in-COVID time period, we hope to cluster tweets based on similarity or correlation into topics that were most trending during the entire duration. Comparing these clusters, we can identify the difference between pandemic and non-pandemic time periods. 

### 4. Considered Potential methods to be applied (as of now):
The data fetched from the online source will never be clean, therefore it will be not easy to analyze or perform the pre-processing easily. We plan to perform below few steps to perform pre-processing:
- Handling missing values, duplicates
- Handling outliers
- Handling multiple languages, for the purpose of this project, we will only consider tweets that are in English
- Stopwords removal, common words that act as noise can be removed as they are not significant for our clustering process
- Vectorization

After cleaning and vectorization, we will create a matrix that contains the tweets, which are free from noise. Then we will use machine learning algorithms to efficiently group the topics that are talking about similar issues or things into a cluster.
We are planning to use a few traditional algorithms along with new trending clustering algorithms like :
- Hybrid Clustering
- Fuzzy Clustering
- Density-Based Clustering 
- Model-Based Clustering 


### 5. Metrics for predicting success: 
We plan to compare our cluster results with the most trending hashtags from that time to identify commonalities. We will be setting the percentage criteria for similarity to ascertain the success of our algorithm. We have identified multiple third party websites to identify top trending tweets from certain time periods. Few of the websites are referenced at the end of the document [1,2].  


### 6. Github link of the Repository:
https://github.com/revanth802/CMPE-255-FA2020-Team6

### References :
1. https://us.trend-calendar.com/
2. https://trendogate.com/
3. https://towardsdatascience.com/the-5-clustering-algorithms-data-scientists-need-to-know-a36d136ef68
4. https://www.datanovia.com/en/blog/types-of-clustering-methods-overview-and-quick-start-r-code/
