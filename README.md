# Seefood: Hotdog, Not Hotdog
## Overview
This project is inspired by the fictional app Seefood created on HBO's Silicon Valley. 
The idea of the app is to work as a simple image classifier to identify an image as either a hotdog or not a hotdog. 
This attempt at classification is built using a 4-layer deep neural network with Relu Activation for the hidden layers and sigmoid for the classification output layer. 

## Set Up/Data
The hot-dog-not-hot-dog folder can be found at https://www.kaggle.com/dansbecker/hot-dog-not-hot-dog/data. There are 500 train samples split between hot dog and non hot dog images. And there are 500 similarly structured test images. The images are resized to 64x64 pixels, which we then flattened into numpy vectors of shape (64x64x3, m=500).
## The Model
The model is derived from an exercise in Andrew Ng's Neural Networks and Deep Learning course from deeplearning.ai. The input layer of the model accepts every pixel of each image, the x dimension of the numpy vector, as each feature -- thus, giving the input layer a dimension of 64x64x64. The next layer has a dimension of 20 units, and the next hidden layer has a dimension of 7 units, each activated by a Relu activation function. The final output layer, with a dimension of 1, activated by a sigmoid function to produce our output. We determined cost using the binary cross-entropy function and then performed gradient descent with a learning rate of 0.0075. We performed a total of 1600 iterations. 
