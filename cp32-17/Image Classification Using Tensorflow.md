* Used a pretrained model to detect objects in an image
* Used Convolution Neural network for accurate image classification using Sequential model by creating matrices of weight called filters to identify complex attributes.
* Used fit function for training.Records loss and accuracy for a given number of epochs and a particular batch size.
* Added activation function sigmoid in model for predicting probability of stop and non stop signs to be in class a or class b
* Decreased overfitting of data through data augmentation
* Created 3*3 size kernels for every image of 32 pixels using 1 and 0 pproach for stop and non stop signs classification
* Model testing by detecting probabilities using predict_generator
* TensorFlow version 2.3.0 is used