## Convolutional Neural Networks for Sentiment Analysis

a tensorflow implementation of the paper [Convolutional Neural Networks for Sentence Classification](http://arxiv.org/abs/1408.5882)

The code is highly based on :
- [Yoon Kim](https://github.com/yoonkim) theano [implementation](https://github.com/yoonkim/CNN_sentence)
- [Denny Britz](http://www.wildml.com) tensorflow [implemetation](https://github.com/dennybritz/cnn-text-classification-tf)
- [abhaikollara](https://github.com/abhaikollara) tensorflow [implementation](https://github.com/abhaikollara/CNN-Sentence-Classification)

This model is slighlty different from the previous ones. There is possibility to
use several pretrained vectors, load a few different datasets and choose
between using the same filter during convolutions for all 
word embedding channels or a seperate one. Finally, provides cross validation 
splits for the datasets used (although, cross validation is not explicitely
implemented). At the moment when assesing on a dev/test set all words that didn't
exist in training set are considered unknown, even when using pretrained vectors...

## Requirements

- Python 3
- Tensorflow 1.0
- numpy

## Running instructions

- change arguments in `conf.py` according to needs 
- replace/change code in `main.py` according to preference
- run code using `$ python main.py`

## Configuration file

Here are several hyperparameters that need to be fixed prior to running
or else the program is going to crash.
Currently there is no possibility to download automatically the
supported datasets or/and word vectors. So, one must download and point to them

## Tensorboard

There is a possibility to check variables/embeddings in tesorboard too
(although not so well implemented) just run

`$ tensorboard --logdir ./runs/`

if your current directory is the code folder. 

## Supported datasets
- [Stanford Sentiment Treebank](http://nlp.stanford.edu/sentiment/index.html) both binary and finegrained.
- [Movie Review Data (MR)](http://www.cs.cornell.edu/people/pabo/movie-review-data/)
- [Large Movie Review Dataset (IMDB)](http://ai.stanford.edu/~amaas/data/sentiment/)

## Supported word embeddings
- [Glove](https://github.com/stanfordnlp/GloVe)
- [word2vec](https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit)
- [fastText](https://github.com/facebookresearch/fastText/blob/master/pretrained-vectors.md)
- [Dependency-Based Word Embeddings](https://levyomer.wordpress.com/2014/04/25/dependency-based-word-embeddings/)


