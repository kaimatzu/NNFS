# Chapter 1 Notes:

## Important terms

### Supervised Machine Learning
- **Definition:** *Supervised Machine Learning* is employed when there is existing labeled data for training purposes.
- **Key Concepts:**
  - **Feature:** An individual attribute or characteristic in the data.
  - **Feature Set:** A group of features, typically represented as vectors or arrays.
  - **Sample:** A specific instance or data point characterized by its feature values.
  - **Target (or Label):** The output assigned to each sample, representing the desired prediction (e.g., "Dog" and "Cat," "Success" and "Failure").
- **Training Data:** The labeled dataset used for teaching the model to associate features with corresponding targets.
- **Objective:** To enable the model to make accurate predictions on new, unseen data by learning patterns from the labeled examples.

### Unsupervised Machine Learning
- **Definition:** *Unsupervised Machine Learning* deals with data that lacks pre-established labels. Instead of predicting outcomes, the algorithm identifies patterns or structures within the data.
- **Components:**
  - **Data Representation:** Unlabeled data is used to discover inherent structures or relationships.
  - **Tasks:** Common tasks include clustering similar data points or reducing dimensionality.
  
### Semi-Supervised Machine Learning
- **Definition:** *Semi-Supervised Learning* combines supervised and unsupervised elements, utilizing a small amount of labeled data and a larger pool of unlabeled data.
- **Benefits:**
  - **Cost-Effectiveness:** Useful when obtaining labeled data is resource-intensive.
  - **Model Training:** The model is trained on the labeled subset and extends its knowledge to make predictions on unlabeled data.
  
### Reinforcement Learning
- **Definition:** *Reinforcement Learning* involves an agent interacting with an environment, receiving feedback in the form of rewards or penalties based on its actions.
- **Objective:**
  - **Optimal Actions:** The agent aims to learn the sequence of actions that maximizes cumulative rewards.
  - **Applications:** Commonly used in game playing, robotics, and autonomous systems.

### Self-Supervised Learning
- **Definition:** *Self-Supervised Learning* is a form of unsupervised learning where the model generates its labels without human annotation.
- **Approach:**
  - **Pretext Tasks:** Involves creating tasks that don't require external labels but guide the model in learning meaningful representations.
  - **Examples:** Contrastive learning, predicting missing parts of the input.

### Transfer Learning
- **Definition:** *Transfer Learning* involves training a model on one task and applying the learned knowledge to a related but different task.
- **Advantages:**
  - **Resource Efficiency:** Efficient use of computational resources, especially with limited labeled data for the target task.
  - **Types:** Feature-based transfer, instance-based transfer, and fine-tuning are common approaches.

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