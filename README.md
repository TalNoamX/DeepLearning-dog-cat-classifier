# Deep Learning classifier

**Project topic:**
Deep learning Project using TensorFlow and NumPy - an image classifier which implements a NN, trained to distinguishes between dog and cat pictures.Features are the pixels of the photos, training set is already labeled photos of either dog or cat, while the testing set is unlabeled photos.

**Abstract:**
CNN is a very popular class of deep learning used mainly for analyzing of visual imagery, with emphasis on image classification. 
In this paper, we'll describe our attempt to build an accurate CNN classifier for dog and cat images using a pretty small data set[1] (6K sized train set, 2K sized validation set and 2K sized test set), and a relatively weak computer system (laptops with basic GPU and only 8GB RAM), and compare its results to basic Logistic Regression and MLP models which we created on the same environment.
The CNN itself is composed of VGG blocks[2], using data augmentation[3] and Dropout as regularization methods.
The coding itself is done in python 3.7, using TF(2.0).Keras framework.
Our best results (on not previously seen images) are little above 92% (test - set accuracy) and 0.92 F-measure.

**Introduction:**
In most cases, trying to solve a problem using Deep Learning methods requires a lot of data to begin with, or at least this is the common believe, train sets are hopefully as big as possible[4], while size and variety of data used for training the model is believed to be crucial to the "strength" of the model[5], this leads most data scientist's to work with "super-computers" which are built to this purpose[6].
But, in our case, we work with laptops which are not strong enough (GPU and RAM wise) to  process a really large data bundles at once, in addition – training the model (even on this not-so-big data set) is VERY slow (even while using data batches and multi-threaded processing), so our data set has to be quite small.
 The point of our research is to show that building efficient CNN's is possible even with small data sets and relatively weak computers, in addition, we compare such CNN's with basic Logistic Regression and MLP.
Lucky for us, CNN models which composed of VGG blocks and use data augmentation, don't require this much of train data[7], so this architecture is perfect for our situation.
VGG blocks emerged for the first time from "Visual Geometry Group" at Oxford University[8], and are now very popular in CNN's, as they believed to be very efficient. 
Classic VGG block is composed of a convolutional layer (with padding to maintain the resolution) with 3X3 sized kernel, nonlinear activation function (as the classic "ReLU" for example), and finally 2X2 max pooling with stride of 2 (for halving the resolution after each block)[8].
Typical CNN architecture using VGG blocks:
 
In our research we found that best solutions to cat and dog classification problems, using VGG blocks – are around 97% of accuracy[10], we haven't got "this good", and stopped around 92% because as already mentioned – time and computation limits.

