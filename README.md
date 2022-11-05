# Wrangle WeRateDog Tweets
### By Jeremy Ikwuje

I'm currently undergoing the Udacity Data Analyst Nano Degree program. Part of the coursework is to gather, assess, clean and analyse tweets from the WeRateDog [Twitter](https://twitter.com/dog_rates) account.

WeRateDog is a popular Twitter handle that post funny dog photos and rate them in tweets. They are over 5000 tweets (mostly dog ratings and retweets) on their timeline. Most of these tweets have recorded thousands of likes, retweets, and replies.

In this report, I will explain how I went about gathering, assessing, cleaning and analysing tweets data from the WeRateDog account.

## Data Gathering
Thank goodness. I didn't really need to gather fresh data from scratch. A dataset was provided by Udacity. The dataset contains about 5000 tweets ratings (with tweet IDs) from WeRateDog. My job was to get additional info (retweets and likes) for each tweet using the tweet ID.

Twitter have an open-closed API (application programming interface) that allows developers to read and write data on its platform. All I have to do is to apply for a developer account and create APIs access keys.

As a software engineer, writing the python code to access the Twitter API and gather extra tweets info from WeRateDoge wasn't a big deal; though I had a little challenge with tweepy. Tweepy is a python package that makes it easy to access the Twitter API. All I had to do was to loop over the dataset (from Udacity) and get the additional info for each tweet using the `tweepy.api.get_status(tweet_id)` method.

To further assess this additional tweet info, I saved each info(in JSON) line by line in a file `tweet-json.txt`. 

## Assessing Data
I access the data virtually and programmatically. This was to check for data quality and tidiness.

Doing that enabled me to spot eight quality and tidiness issues with the dataset. Some of the issues are:

- some tweets info were not needed e.g `source`, `reply_status_id`, and others.
- some columns in the dataset (provided by Udacity) had to be renamed
- also some tweets are not dog ratings but retweets from other Twitter accounts; since we are only dealing with ratings, we had to remove retweets from the dataset.

Assessing the data was tough for me: I had to assess and understand the data properly, taking a lot of time. In fact, the entire wrangling process was hard.

## Cleaning Data
Cleaning the data requires I define the issue, write code for it; and then test it.

Coding isn't that hard for me anymore. And there is a google result for nearly every coding problem.

Eight quality issues and two tidiness were cleaned successfully.  

## Analysis
Further details about the project analysis and visuals can be found on my blog. 

...

One thing I will love to mention is that I used a web tool called DeepNote for this project, it was my first time and I love it. I was able to discover this tool because my Windows PC (with Anaconda installed) wasn't with me so I had to use my Chromebook.

Thanks for reading.