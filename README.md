## Introduction
An application that predicts the price of an item given its image and a short description.

## Purpose
* Allows a merchant to determine what price they should sell their products for, without having to do any prior research.
* Allows a consumer to determine the appropriate price for an item, without having to do any prior research.
* Allows a merchant to choose which image, in the consumer's eyes, is of greatest value.

## Pipeline
![alt text](https://user-images.githubusercontent.com/13950182/30246098-14ab44be-95be-11e7-9d7f-849aa3a84092.png)

#### R-CNN
A pre-trained neural network, the BVLC Reference RCNN ILSVRC13, was used and evaluated with the Caffe framework. 4096 float features are obtained for each image by taking the output of the second fully connected layer (FC7).

#### Count Vectorizer
The Scikit-Learn CountVectorizer module was used, which was configured to do the following:
* Word tokenization, using the nltk word_tokenize function
* Stopword removal, using the default English stopword set
* Only selecting words with document frequency >= 5
* Binary output features

#### Regression Model
A gradient boosted decision tree model was used, namely the sklearn.ensemble.GradientBoostingRegressor module, with the following parameters:
* 500 estimators
* 

## Contributors
* Stephanos Kantzidis
* Jagadish Rangrej
* Haoran Zhang

## Acknowledgments
* Data provided by [Julian McAuley of UCSD](http://jmcauley.ucsd.edu/data/amazon/)
