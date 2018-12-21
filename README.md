# Arabic(Egyptian) ID card's digits dataset

This repo contains a dataset of 10,603 samples of printed Arabic numeral digits used in Egyptian ID cards - collected to be used as part of an Arabic OCR system.

### Training

A set of 10,000 samples divided into 10 classes for digits 0, 1, 2, 3, 4, 5, 6, 7, 8 and 9. Each class has equal number of 1000 samples. Each sample is saved so that the background is black (has values close to zero) and the digits pixels are white (have values close to 255). This is important because the default color of the Arabic numbers found in Egyptian ID cards is black, which means you need to invert the digit's' colors before using a model trained on this dataset.

Data augmentation has been done to this dataset on a smaller subset of samples varying the scale and orientation of the original samples to produce a sufficient number of samples.

### Testing

A set of 603 samples are used for testing. Some of these digits have been used for the augmentation of the training dataset which may lead to think it's not sufficient for testing the accuracy of the model however, experiment has shown that this test set shows very close results to new test samples fed to a model tested on this test set.

### model_A.ipynb

A Jupyter notebook of the model trained on this dataset. However this is not the final model that shows the desired accuracy.

### model_a.h5

The saved model.
