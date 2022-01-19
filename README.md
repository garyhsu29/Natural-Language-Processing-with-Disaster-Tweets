# Kaggle competition - Natural Language Processing with Disaster Tweets
#### [Slide for the project](https://github.com/garyhsu29/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Natural%20Language%20Processing%20with%20Disaster%20Tweets.pdf)
 
### Attempt 1: Use Keyword and Location as feature
- Keyword Preprocessing: Remove URL encoding
- Location Preprocessing: Remove the Nation/State, only keep the first part of location information
- Results: 
    - Model 1: [Decision Tree (71.80% validation accuracy)](https://github.com/garyhsu29/Natural-Language-Processing-with-Disaster-Tweets/blob/main/keyword_location_experiment.ipynb)
    - Model 2: [Support Vectior Machine (73.46% validation accuracy)](https://github.com/garyhsu29/Natural-Language-Processing-with-Disaster-Tweets/blob/main/svm-classifier.ipynb)
- Kaggle Leaderboard: 788/868

### Attempt 2: Use Tweet and Location as feature
- Preprocessing: Different model need to apply different preprocessing steps for tweet
- Paper Research: 
   - [TWEETEVAL](https://arxiv.org/pdf/2010.12421.pdf)
   - [BERTweet](https://arxiv.org/pdf/2005.10200.pdf)
- [Raw Transformers model (79.19% validation accuracy)](https://github.com/garyhsu29/Natural-Language-Processing-with-Disaster-Tweets/blob/main/Transformers_for_tweet_analysis.ipynb)
- BERT related [Models:](https://github.com/garyhsu29/Natural-Language-Processing-with-Disaster-Tweets/blob/main/bertweet-analysis.ipynb)  

|Model Name| Paper |Validation Accuracy|Test Accuracy(Kaggle Leaderboard)| 
|-----|--------|----|------|
|bertweet-base| [BERTweet](https://arxiv.org/pdf/2005.10200.pdf)|84.17%|84.80%|
|bertweet-covid19-base-uncased| [BERTweet](https://arxiv.org/pdf/2005.10200.pdf)|84.24%|82.08%|
|bertweet-large | [BERTweet](https://arxiv.org/pdf/2005.10200.pdf)|84.36%|82.27%|
|twitter-roberta-base |[TWEETEVAL](https://arxiv.org/pdf/2010.12421.pdf)|83.44%|81.77%|
- Kaggle Leaderboard: 48/868