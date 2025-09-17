# Pandas2
1 Problem 1 : Article Views I	(	https://leetcode.com/problems/article-views-i/  )
Solution:

import pandas as pd

def article_views(views: pd.DataFrame) -> pd.DataFrame:

   df = views[views["author_id"] == views["viewer_id"]]
   df.drop_duplicates(subset = "author_id", inplace = True)
   return df[["author_id"]].rename(columns = {'author_id' : 'id'}).sort_values(by = 'id')
2 Problem 2 :Invalid Tweets	(	https://leetcode.com/problems/invalid-tweets/ )
Solution:

import pandas as pd

def invalid_tweets(tweets: pd.DataFrame) -> pd.DataFrame:
   return tweets[tweets["content"].str.len() > 15][["tweet_id"]]










