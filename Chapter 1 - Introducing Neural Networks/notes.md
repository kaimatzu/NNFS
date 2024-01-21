# Chapter 1 Notes:

## Important terms
### Supervised Machine Learning
- *"Supervised Machine Learning"* is used when you have pre-established and labeled data that can be used for training.
- Data used for training is called a *"Feature"*.
- A group of Features makes up a *"Feature Set"* (represented as vectors/arrays).
- Values of a Feature Set can be referred to as a *"Sample"*.
- *"Classifications"* or *"Labels"* are the *targets* that the network will assign output values to (e.g. "Dog" and "Cat", "Success" and "Failure", etc.)

## About Neural Networks
A single neuron by itself is relatively useless, but, when combined with hundreds or thousands (or many more) of other neurons, the interconnectivity produces relationships and results that frequently outperform any other machine learning methods.

We have no idea why they reach the conclusions they do. We do understand how they do this, though. 

[[More reading on the *Emergent Properties* of Neural Networks]](https://guava.physics.uiuc.edu/~nigel/courses/569/Essays_Spring2018/Files/khan.pdf)

A typical neural network has thousands or even up to millions of adjustable *"Parameters"* (weights and biases). This can be thought of as a highly complex equation/function with millions of variables. The goal of training a Neural Network is to find the optimal combination of these parameters in order to solve a problem (in this case, classification of data).

One major issue with training Neural Networks is *"Overfitting"*, when the algorithm only learns to fit the training data but doesn’t actually *understand* anything about underlying input-output dependencies. The network will perform perfectly on the training data given but will perform horribly on actual data.

The fix is *"Generalization"*. You use “in-sample” data to train a model and then use “out-of-sample” data to validate the Neural Network.

To train these neural networks, we calculate how “wrong” they are using algorithms to calculate the error (called *"Loss"*), and attempt to slowly adjust their parameters (weights and biases) so that, over many iterations, the network gradually becomes less wrong.

## Formula for a single epoch:
### Output of a neuron before activation
- output = sum(inputs * weights) + bias
### Apply an activation function
- output = activation(output)