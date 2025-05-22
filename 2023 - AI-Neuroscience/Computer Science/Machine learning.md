Machine learning is a field of [[Computer Science]] that is concerned with systems that are able to *learn from* [[Data]].

# Algorithm classification

As of 2022 there are 3 major categories *Supervised*, *Unsupervised* and *Reinforcement*learning methods. Each one of those have their own strenghts and limitations. There is a fourth Category which combines the best features of all worlds called *Semi-supervised* learning.
![[Pasted image 20221017141357.png]]


## Supervised Learning
Supervised learnng methods use labeled [[Data]] to train the model. 
What is labeled Data? Labeled data is simply data that has been categorized by someone or something else. For example we could have images of numbers and the label (name) is each number (see sample below).
![[Pasted image 20221017142901.png]]

These methods force the model to *fit* the data with the label, so future data can be processed and categorized with better accuracy.

Here you use data from the past to train the model and make predictions or classify  new data.

### Use cases
- Classification
- Prediction or Regression

Sample: We could train a model to classify spam emails. First we will need to fetch a good number of spam and legitimate emails, label them and train the model to classify a spam vs a legit email.

### Famous Algorithms
- Linear Regression
- Support Vector Machines (SVM)
- Logistic Regression
- Decision Tree
- Neural Networks


## Unsupervised learning
Unlike supervised learning, unsupervised learning doesn't require the data to be labeled, instead these methods find patterns in the data itself without any human intervention. 
It is often used for exploratory data analysis, customer segmentation, association and dimensionality reduction (autoencoders).
![[Pasted image 20221017145739.png]]

### Use Cases
- Data clustering (classification)
- Association (discover connections between data points)
- Dimensionality Reduction
- Anomaly detection (detect outliers)

### Famous Algorithms
- k-means
- Hierarchical clustering
- Gaussian Mixture Model
- PCA
- Autoencoders

In terms of classification, supervised learning models are way more accure, simply because of the pre-work done to label the data manually. If we get to auto-label the data somehow, unsupervised learning will definetly take over due to the amount of data we would be able to process without needing to label it.

## [[Reinforcement learning]]
Reinforcement learning introduces 4 new concepts to the learning loop, which are **agent** and **environment** to perform an **action** (output) and maximize a **reward**.

It also continuosly adapts to new data, so the agent is learning at the same time it is choosing an action.

These types of algorithms work best when the problem is properly framed. A common practice is to gamify the problem and choose a proper reward to maximize, this way the agent (the model) will learn the best route to solve the problem.

![[Pasted image 20221017152406.png]]

Reinforcement learning is often used for high dimension problems, or super hard problems, like self-driving cars, trading strategies, gaming, real-time bidding, robotics, 

### Use cases
- Robotic arm manipulation
- Self-driving cars
- Bot in games
- Real-time bidding price
- Server scale optimization

### Famous Algorithms
- Q-learning

## Semi-supervised Learning
Say you want to create a cat/doc classifier and you have 1,000,000 images, but you only have 300,000 labeled samples, here is what semi-supervised leanring does
1. Trains a model with the labeled data
2. Label de remaining data with the trained model (this is called pseudo-labeling)
3. Retrain the model with the 1,000,000 images that are now labeled
4. model ready
