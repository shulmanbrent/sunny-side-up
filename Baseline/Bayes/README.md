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
    -h: print this help message and exit (also --help)
    -f txt_file: specify path for txt file containing tweet features
    
    --bernoulli: specifies the use a Bernoulli Naive Bayes classifier from the nltk's scikit learn integration
    --multinomial: specifies the use a Multinomial Naive Bayes classifier from the nltk\'s scikit learn integration'
    --gaussian: specifies the use a Gaussian Naive Bayes classifier from the nltk's scikit learn integration
    --help: prints help message and exit (also -h)
    
A sample output of this pipeline looks like this:
```
Opening CSV file...

Extracting Features...
CSV file opened and features extracted
Data split into sets
Classifier trained
Evaluating accuracy and other features

Classifying test data...
Test on 159998 instances

accuracy: 0.775740946762
pos precision: 0.823663853727
pos recall: 0.702179479173
neg precision: 0.740086329053
neg recall: 0.84942389251
Most Informative Features
                 me..its = True              pos : neg    =    107.0 : 1.0
                  Farrah = True              neg : pos    =     65.1 : 1.0
              Banksyart2 = True              pos : neg    =     53.7 : 1.0
             shareholder = True              pos : neg    =     48.3 : 1.0
             condolences = True              neg : pos    =     44.7 : 1.0
                 McMahon = True              neg : pos    =     43.0 : 1.0
                     447 = True              neg : pos    =     42.4 : 1.0
                 sadface = True              neg : pos    =     42.3 : 1.0
                    Poem = True              pos : neg    =     41.8 : 1.0
                  triste = True              neg : pos    =     39.0 : 1.0
              recommends = True              pos : neg    =     38.6 : 1.0
                 *cries* = True              neg : pos    =     37.9 : 1.0
               gratitude = True              pos : neg    =     37.7 : 1.0
                     vip = True              pos : neg    =     37.5 : 1.0
                 saddens = True              neg : pos    =     35.0 : 1.0
                    Died = True              neg : pos    =     34.1 : 1.0
                    sadd = True              neg : pos    =     33.8 : 1.0
           Disappointing = True              neg : pos    =     33.7 : 1.0
                  boohoo = True              neg : pos    =     32.1 : 1.0
             heartbroken = True              neg : pos    =     30.8 : 1.0
```
