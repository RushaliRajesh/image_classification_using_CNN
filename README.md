# image_classification_using_CNN
The objective of this project is to classify the images of CATS and DOGS using a CNN model 

# dataset
The training and testing dataset that was used for this project consisted of various images of dogs and cats. These images were of size(375,500).
for more reference on loading dataset, click [here](https://github.com/RushaliRajesh/image_classification_using_CNN/blob/master/scripts/loading%20data.md)

# Data preprocessing                 
This is the most important step as we prepare the data for training and testing. First we reshape all the images of training and testing dataset such that all of them are of same shape.
The training dataset is then shuffled so as to make the training better. If not shuffled, the machine trains on all the images of cats first and the on the images of dogs which becomes a hinderence to better training.
[reshaping_data](https://github.com/RushaliRajesh/image_classification_using_CNN/blob/master/scripts/data%20preprocessing.md) &
[shuffling_data](https://github.com/RushaliRajesh/image_classification_using_CNN/blob/master/scripts/training_data_shuffling.md)

# CNN model
After converting the training data into their respective [one hot encoded values](https://github.com/RushaliRajesh/image_classification_using_CNN/blob/master/scripts/converting%20to%20one%20hot.md), we create a sequential model using tensorflow backend and keras.
The model consists of 2 Conv2D layers with MaxPool layers and 2 FC layers.
![Screenshot (29)](https://user-images.githubusercontent.com/53039674/83637361-253b3900-a5c5-11ea-854e-53b9a4145a27.png)

# Compiling and Fitting Data
We first compile the model and then fit in onto the training data with suitable number of epochs. We can also give a certain batch size if the dataset is too huge.
Here in the fitting of data we use the test data as the validation dataset.[evaluation](https://github.com/RushaliRajesh/image_classification_using_CNN/blob/master/scripts/compiling_fitting.md)
