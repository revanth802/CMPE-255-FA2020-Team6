## CMPE-255-FA2020-Team6

# Clustering Based Behavioral and Social Insights w.r.t Pandemic 

### PROJECT TEAM MEMBERS (WITH GITHUB USERNAMES):
- Revanth Krishna Maddula- revanth802
- Harshit Malwiya- harshitmalwiya
- Priyanka Sharma- Priyanka1891
- Kailash Nath Tallapragada- kailashnath979

### Data Source:
The data we will be using is the real-time tweets fetched from Twitter. We will get the tweets using “Tweepy”, an API for twitter-streaming from where we can access the tweets which we import into a pandas data frame. After this, we can perform the required steps to proceed with the project.
We will be focusing mainly on the tweets from the year 2019 and 2020 for this project. The link to the Tweepy API must be done by getting access from the official twitter developers website specified: https://developer.twitter.com/en

### Description of the problem we are investigating:
The COVID-19 Pandemic has shifted and changed our day to day lives in a very exponential manner. While it is difficult to measure this due to lack of everyday data of people’s lives, social media can provide us little insight into people’s emotions, spending habits, and actions.

## Preliminary Analysis

### Summary of Data
The data set was generated using official twitter API and fetching tweets for the year 2019 and 2020 month-wise. Since twitter has a well managed environment for handling and providing data, it provides multiple options to fetch, filter and collect the data.

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
Data set was filtered using the following parameters : 
- Start Date
- End Date
- Retweet
- Language

### Data Cleaning
Since twitter has a fixed format on storing user data and tweets, the dataset was clean of human induced errors. Tweets have a fixed length of 280 characters. Personal user information is mandatory with built-in validations. 
We performed cleaning as per the following steps : 
- Removed spam tweets
- Removed duplicate tweets
- Removed retweets
- Removed emojis and other graphical data
- Removed Http/Https
- Removed any numeric data (if present) in tweets
- Removed any kind of special words
- Verified Users





