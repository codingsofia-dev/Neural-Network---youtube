# Neural-Network from a youtube-video


In this project, we wanted to follow the youtube-video by Samson Zhang: **Building a neural network FROM SCRATCH (no Tensorflow/Pytorch, just numpy & math)**. 
- Link: https://www.youtube.com/watch?v=w8yWXqWQYmU.

In the youtube-video Samson Zhang tackles a ‘digit-classification’ problem. He builds a neural network that classifies what digits are written in a image of handwritten digits. 

Each image is 28 x 28 pixels. Each pixel has a value between 0 (black) and 255 (white), and each image is converted into a matrix of numbers. This matrix represents the handwritten number. 


## Important information
We used the same dataset as the youtube-tutorial (from Kaggle).
- Link: https://www.kaggle.com/competitions/digit-recognizer/overview

It is licensed under: CC BY-SA 3.0. 
- https://creativecommons.org/licenses/by-sa/3.0/

**This repository contains our implementations of a neural network built while following Samson Zhang's video. It is a learning exercise, not original work and we do not claim any of the code as our own! **

The comments in the code are our own. 
We decided to code on our own laptops instead of the notebook-tutorial on Kaggle as shown in his video, as we do not have experience with Kaggle. 

## Background information
Both of us took the course ‘IN3050 - Introduction to artificial intelligence’ and machine learning, as well as the course ‘IN1160 - Introduction to machine learnin’ at the University of Oslo. Although we have already built different neural networks, we wanted to refresh our memory! We found this youtube-video and decided to follow along. **The code is not ours!**



## What is a neural network?
A neural network is supposed to mimic our brains. The brain consists of many neurons that work together in order to function fast and effectively. 

The neural network is an extension of the perceptron: a simple linear model. It consists of weights and inputs and an activation function in order to produce an output. The perceptron uses a ‘step function’ when computing the output. 
the inputs are the features we pass into the model: x
the weights control how much influence each input has on the output: w

The weights are multiplied with the features and a bias is added. The best way to think of what a bias does is by thinking of fitting the line: y = mx + b.
- y is the value for a given x
- m controls how steep the line is
- b controls where the line crosses the y-axis

If the b is 0, you are forcing the line through 0, but you might not want y = 0, when x = 0. If the bias is 0, you are forcing the model to pass through the origin, (0,0) and this can be unrealistic for real-world relationships. 

The perceptron is mainly used for binary classification (output is 0 or 1), and we use the step-function to convert our numerical value, z, into a binary one. 

A neural network has an input layer, one or many hidden layers, and an output layer. Each layer is made up of nodes. The does in the hidden and output layers behave like the classical perceptron: computes a weighted sum + bias and applies an activation function. 

In the code, the ReLU function is used in the first hidden layer and a softmax-function in the output layer. To explain them shortly:
ReLU makes sure that each value is 0 or positive
softmax gives values between 0 and 1 (like probabilities)

We have two stages: forward pass and backpropagation. In forward pass, we initialize the weights and the bias and make predictions. But these weights are most likely not the most optimal values, and through backpropagation and gradient descent we update these parameters. We can track how well the model is doing with the accuracy score. 

## RESULTS
The code has an accuracy of about 84%. In the third, test-prediction we can see that the model didn't predict correctly (predicted 1 instead of 7). 
