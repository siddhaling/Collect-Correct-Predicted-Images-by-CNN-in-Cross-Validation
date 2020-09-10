# Collect-Correct-Predicted-Images-by-CNN-in-Cross-Validation
Collect all the correctly predicted images by CNN during cross validation

***********************************************************************************************************************
This is a python code to collect all the correctly predicted images by CNN during cross validation
***********************************************************************************************************************

Package Version\
python 3.6.8\
pandas 0.24.1\
Keras 2.2.4\
skimage 0.16.2

During the analysis of the CNN and to improve its performance\
many times it is important to know correctly predicted images.

The input to this code is the path to a directory containing images.\

### How to run this python code?

To run the correctPredictedImagesByCNN.py, please provide the path to the director containing images to imFolder.\
As an example, a few images are kept in the folder 'images'.\

Few samples are kept here for complete dataset please refer\
https://mcrlab.net/research/mvsa-sentiment-analysis-on-multi-view-social-data/

The ground truth i.e class label information is to be kept in the file groundTruthMv_a.txt.

Initially the class label information is read and stored in a dataframe.\
All the paths of the images from the given directory are read and a list of paths to images is prepared into allImsPaths.\
This list is then refined to remove the paths which are not part of ground truth file.

A directory is created by storing images content and class label of the image. The prepared directory is called as imDbDict.\
Five folds of the data are created using StratifiedKFold()\
The CNN model is created using the function buildModel() and compiled on the given parameters.
A training set consisting of images of four folds is created and one fold for test images.\
The CNN is trained on four folds and tested on one fold.\
The CNN model is trained using fit() function on training set.\
The predict_classes() function is used to determine predicted class lables by CNN.\
Using the function selecteCorrectPredIms() a list is prepared consisting of all the correctly predicted images from the test fold.\
This list is most useful to understand and to improve the performance of the CNN.\

# Further Projects and Contact
www.researchreader.com

https://medium.com/@dr.siddhaling

Dr. Siddhaling Urolagin,\
PhD, Post-Doc, Machine Learning and Data Science Expert,\
Passionate Researcher, Focus on Deep Learning and its applications,\
dr.siddhaling@gmail.com
