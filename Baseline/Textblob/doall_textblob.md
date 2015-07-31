

    import os, sys
    sys.path.insert(0, '../Textblob')
    sys.path.insert(0, '../..')
    from datasets import sentiment140
    from textblob import TextBlob
    from textblob_evaluator import textblob_evaluator


    tweet_list = sentiment140.load_data()


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

