# Natural Language Processing r/wallstreetbets and r/investing
## Tyler Zarnik
   
## Problem Statemant

> I am working with a team on behalf of Reddit.com to find if wallstreetbets is a problematic sub that should be removed from the platform due to hatespeech. We will be comparing this to a subreddit with a very similar focus, r/investing to see if the subreddits can be truly and quickly distinguished from one another based on the laguage used.

## Executive Summary

The goal of this project is to be able to train a model that is able to distinguish posts from two different subreddits where one commonly has hate speech. 

Reddit is a website that often want to present itself as platform for many different types of communities. However, as recent politcal trends have started to become more polarized and even pereptuated by online communities, Reddit is looking to cull this behavior.

Ultimately, we were able to find models that were able to explain 30% more of the posts than a simple null model and tease out the most used words for the subreddits. It also was able to identify some of the most problematic words that specifically and statistically indicated a post from wallstreetbets.

This will  be accomplished by collecting over 5 months of data from the two subreddits. We will use natural language processing libraries to clean through our data sets including stemming and lemmatizing the words. We will also remove any items that have missing vales in the post title or post description as this will be our primary determining factor. We will want to employ a model that does have some explanatory power in regards to its features or coefficients, so that the model is able to tease out which words are specific for determining each subreddit. In addition, we will clean out any outright profanity and will use the better_profanity library to take out any common profanity or slurs.

### Contents:

- [Data Dictionary](#Data-Dictionary)
- [Imports](#Imports)
- [Data Collection](#Data-Collection)
- [Data Cleaning & EDA](#Data-Cleaning-&-EDA)
- [Preprocessing & Modeling](#Preprocessing-&-Modeling)
- [Evaluation and Conceptual Understanding](#Evaluation-and-Conceptual-Understanding)
- [Conclusion and Recommendations](#Conclusion-and-Recommendations)

## Data Dictionary 

|Feature|Type|Dataset|Description|
|---|---|---|---|
|subreddit|object|df,wsb,inv|Identify Subreddit|
|Title|object|df,wsb,inv|Uncleaned Post Title Data|
|Selftext|object|df,wsb,inv|Uncleaned Post Description Data|
|t_tok|object|df,wsb,inv|Cleaned Tokenized Titles|
|st_tok|object|df,wsb,inv|Clean Tokenized Selftext|
|cleaned_tok|object|df|Concateated from st_tok and t_tok|

## Data 
>./data/full_wsb_inv.csv

>clean_inv.csv

>clean_wsb.csv

>clean_wsb_inv.csv

>df_inv.csv

>df_wsb.csv

>dirty_inv.csv

>dirty_wsb.csv

>dirty_wsb_inv.csv

>full_inv.csv

>full_wsb.csv


## Conclusion and Recommendations
While the graph earlier indicated that the most common words used between the subs were innoculus, our model was able to tease out some very problematic results. Despite these words getting through the filter, this would likely indicate that there may be a hostile userbase and hate speech involved here or at the very least extremely distasteful and problematic ways of insulting other users in a joking way. However, joking is always a thinly excuse for that type of behaviour and should rarely if ever be accepted. Our model although not always able to identify the difference between the posts at only an 84 percent accuracy, still performs well above our baseline model of 50 percent. Our model was able to tease out which words and posts are problematic. Our coefficients were also extremly high in many circumstances.

While their is a large amount of evidence here, more would be needed in terms of looking at all user comment data. In addition, we would need to manually review many of these posts that are being teased out by our models. Although this speech is unacceptable, Reddit is a website that tries to maintain an environment that is not inherently toxic but also allowing a certian modicum of a wide array of speech that is also not advocating violence.