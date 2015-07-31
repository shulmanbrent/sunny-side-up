# Bayesian Classification

This folders contains a NLTK/Naive Bayes implementation for analizing the sentiment of the Stanford140 dataset.

To run the sample pipeline type this into the commandline 
```
> python Sentiment140_NB_Pipeine.py
```
Without any flags, the Pipeline uses NLTK's implementation of Naive Bayes. It will first download the Sentiment140 dataset using the ```sentiment140.load_data()``` function from within the datasets directory (If the file has already been downloaded, this function will just access it in from with the ```/datasets/.downloads``` folder  
