# Covid_19_Tweets
NLP Tweets Sentiment
Introduction
At present, there is an ongoing outbreak of a new virus which is an infectious disease commonly known
by the names of coronavirus or COVID-19. This new virus is mainly transmitted through droplets when
an infected person coughs, sneezes or touches surfaces such as table, doorknobs and handrails [1]. The
spread of COVID-19 has impacted people’s lives worldwide. It was declared by world health organization
WHO as pandemic on 11 March 2020[2].
Social media plays an important role in our life as it links people with the outside world. It offers a way
for the people to showcase their lives, free to debate and share their opinions about any events easily
and on their terms [3]. The topic of coronavirus has been one of the most widely discussed topics on
social media such as Twitter, Facebook and Instagram [4]. The main aim of this project is to perform a
sentiment analysis which is a system used for text analyses that combines natural language processing
and machine learning techniques to assign weighted sentiment to entities, topics, themes and
categories within a sentence or phrase. This sentiment analysis is performed on the discussion of people
regarding COVID-19 on Twitter in order to investigate their sentiment /feeling about Coronavirus.
Data
The datasets required for this project are obtained from Kaggle, the first dataset consists [5] of 179108
records and 13 columns, it’s a collection of tweets containing hashtag (#covid-19 and #coranvirus) which
are collected using Twitter API and a Python script. This Dataset set is unlabelled. The second dataset [6]
consists of tweets from India on topics of coronavirus, covid-19 and lockdown which are collected
between March 23, 2020, and July 15, 2020. These tweets of users from India are further classified into
four types of emotion of fear, sad, anger and joy.
 Datasets Exploration
Before getting into Data preprocessing of Tweet data, data exploration has been done in order to
explore the data and check what the first dataset look like.

Preprocessing of Tweets Data
Pre-processing of data is one of the important steps before the data is available for analysis as most of
the text data available on social media is extremely unstructured, has typos, poor grammar, spelling
mistakes, contains unwanted stop words, URLs and special characters [7]. Some of the steps involved in
data pre-processing are as follows:
Conversion of Emoticon and emojis into words: Since we are doing sentiment analysis emoticon and
emojis give us some valuable information so removing or eliminating them might not be a good solution
[8]. Hence the only method to use these emojis and emoticon is to convert them into words by using a
dictionary obtained from GitHub [9]. As can be seen in Figure 16, UNICODE_EMO and EMOTICONS were
imported from emo_uniode library and then two methods were made for the conversion of emoticons
and emojis and these two methods were applied to the text column which contains the tweets data of
the users in coronavirus regards

Removal of URLs: URLs and hyperlinks also does not hold any meaning for the sentiment analysis, so it
should be removed.
Removal of punctuations, numbers, special characters and others: The text column which contains the
tweets is not a clean data, these tweets might contain @ symbol, hyperlinks, RTs, numbers,
punctuations, numbers and hashtags, these are also necessary to remove as they do not contribute to
sentiment. Which is done by creating a function to remove all that is mentioned above and then
applying this function to the text column.


Removal of Stop-words: Stop words are the most common words that do not add any value to the
meaning of the document such as “the”,” is”,” in”, “at” etc. This step of removing stop words is done by
importing stop words from nltk.corpus library and applying it to the cleaned text.


Sentiment Analysis
The tweet data which consists of 179108 records is distributed into three sentiments of positive,
negative and neutral. To view the numerical distribution of these three categories the value_counts()
method is used to view the distributions of each label. As can be seen from Figure 25, 46% of the tweets
have neutral sentiments followed by 30% positive and 24 % negative sentiments.

![alt text](https://github.com/Mobiee/Covid_19_Tweets/blob/main/screenshots%20/barchart1.png =200x200)

After checking the distribution of sentiments from the tweets, the distribution of sentiments amongst
top 5 countries are also explored, as shown in Figure 26 neutral sentiment has the highest distribution in
tweets from Australia, United States, United Kingdom, Canada and India followed by positive and
negative sentiments respectively.

![alt text](https://github.com/Mobiee/Covid_19_Tweets/blob/main/screenshots%20/barchart2.png =200x200)
