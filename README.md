# Business Ambience Classifier
Ambience refers to the general feel/atmosphere of a business.
In this project we consider a finite set of ambiences: intimate,
hipster, divey, touristy, upscale, trendy, and casual. These are based
on the ambience attributes that Yelp uses.

## Classifier Details
This classifier is a One-vs-Rest Classifier that uses LinearSVC to separate individual classes
from the rest of the set. It is trained using supervised learning.
The features are the tf-idf values of the reviews for a business.The labels are sourced from
[Yelp's Dataset](https://www.yelp.com/dataset_challenge) which contains 2.2M
reviews for 77K businesses. There are definitely some shortcomings in the dataset for my needs.
For example, the dataset contains reviews from only a handful of cities. This can limit the
number of businesses from certain ambiences (for example, most of the touristy businesses are
in Las Vegas).

## Word Clouds
To visualize the relative weights of word features, I used this
[Python Word Cloud](https://github.com/amueller/word_cloud)
library. The strongest signals are probably fairly predictable(for humans) but there are some
interesting words. For example, 'lounge' is a fairly strong signal for an 
upscale business, likewise for 'sake' and trendy businesses.

## Code
[Notebook](http://nbviewer.jupyter.org/github/kennzoid/business-ambience-classifier/blob/master/business_ambience_classifier.ipynb)

All the code used in this project are contained within the Jupyter Notebook. I suggest viewing 
it through Jupyter's nbviewer web app (link above).
