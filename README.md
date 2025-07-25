# Image Classificaion Model Using Tensorflow

This program uses machine learning concepts to identify patterns in an image dataset, and classify the image after training. The program was originally designed to obtain the dataset via an online resource, but has since been changed to utilize a local dataset. Data for this model can be found in the 'data' directory, and should a user like to change the model to use their own dataset, they can by simply changing the photos in the 'data/fireAlarmPictures' and 'data/firstAidPictures' directories.

This model works by using Tensorflow to create a convolution neural network. The program scales the data down before sending it into the neural network, where a ReLu activation function is used to introduce non-linearity. The final output neuron uses a sigmoid activation function, as this is helpful for scaling the output from 1 to 0. In this program, an output less than 0.5 means the image has been identified as class 1 -- in this case, a fire alarm. And an output above 0.5 means the image is class 2, a first-aid kit. The program then shows the user how accurate and efficient the model was in training, before exporting the model as an h5 file.

In my testing, the model performed well with 20 epochs of training, and its results can be viewed in the 'modelTrainingPerformance' directory, or below:

![accuracyGraph](modelTrainingPerformance/Accuracy.png) ![lossGraph](modelTrainingPerformance/Loss.png)

I should note for functionality that this program uses the following interpreter and library versions:

Python 3.9

TensorFlow 2.10.1

OpenCV 4.10

NumPy 1.26.4

Pillow 10.4

MatPlotLib 3.9.1
