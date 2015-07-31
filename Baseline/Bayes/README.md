# Bayesian Classification

This folders contains a NLTK/Naive Bayes implementation for analizing the sentiment of the Stanford140 dataset.

To run the sample pipeline type this into the commandline 
```
> python Sentiment140_NB_Pipeine.py
```
Without any flags, the Pipeline uses NLTK's implementation of Naive Bayes. It will first download the Sentiment140 dataset using the ```sentiment140.load_data()``` function from within the datasets directory (If the file has already been downloaded, this function will just access it in from with the ```/datasets/.downloads``` folder.

Optional flags include:
    Usage: doall.py [-i file | -h]
    Options and arguments:
    -h\t\t: print this help message and exit (also --help)
    -f txt_file: specify path for txt file containing tweet features
    
    --bernoulli: specifies the use a Bernoulli Naive Bayes classifier from the nltk's scikit learn integration
    --multinomial: specifies the use a Multinomial Naive Bayes classifier from the nltk\'s scikit learn integration'
    --gaussian: specifies the use a Gaussian Naive Bayes classifier from the nltk's scikit learn integration
    --help\t\t: prints help message and exit (also -h)
