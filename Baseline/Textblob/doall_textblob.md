

    import os, sys
    sys.path.insert(0, '../Bayes-NLTK')
    sys.path.insert(0, '../Textblob')
    from import_stanford_twitter import open_stanford_twitter_csv
    from textblob import TextBlob
    from textblob_evaluator import textblob_evaluator


    tweet_list = open_stanford_twitter_csv('/Users/bretts/Documents/Preparing_The_Torch/StanfordTweetData/training.1600000.processed.noemoticon.csv')


    tweet_list = [(TextBlob(tweet), sent) for tweet, sent in tweet_list]


    textblob_evaluator(tweet_list)

    Classifying test data...
    Test on 1600000 instances
    --------------------------------
    accuracy: 0.622605625
    pos precision: 0.640524018218
    pos recall: 0.55885
    neg precision: 0.608740045831
    neg recall: 0.68636125



    
