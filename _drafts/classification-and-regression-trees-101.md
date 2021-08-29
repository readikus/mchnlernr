---
title: Classification and Regression Trees (CART) 101
description: In this article we will look at the use of classification and regression trees for solving machine learning problems.
date: 2021-08-19
tags:
  - decision trees
  - algorithms
  - scikit-learn
  - visualisation
layout: layouts/post.njk
---

## Overview

Classification and regression trees are like flow charts that allow us to reason about some input values and produce a classication or regression as a result.

Each node of the tree is a test on an attribute - for example, `age > 21` and each branch represents an outcome from the test. Terminal nodes represent the class labels - for example, if we were trying to detect spam emails, our nodes would be testing various factors, such as if certain words are included in the text, and the terminal nodes will tell us if we predict the email is spam or not spam.

In decision analysis, a decision tree can be used to visual represent the decisions being made. This is really important when we want to explain _why_ a machine learning algorithm made a particular classification.

## Advantages of CART

* Simple to understand, interpret and visualise
* Variable screening and feature selection
* Handles numerical as well as categorical data
* Minimal effort for data prepartion
* Non linear parameters do not affect the performance

## Disadvantages of CART

* Overfitting - over complex trees that do not generalise the data well.
* Variance - Pro to small variations in the data producing completely different trees. Handled by bagging and boosting.
* Greedy algorithms can not guarantee returning the optimal decision tree. Greedy algorithms make decisions that seem to be the best fit for that data, so it finds a local optimum rather than globally. See our [summary on random forest](./random-forest-101) for addressing this issue.
* Decision trees learners create biased trees. For example, predicting pauses in text-to-speech, most of the time we do not pause between words, so the data needs to be balanced to better represent the classes.

## Applications of Decision Trees

* Whehter a customer will pay his renewal premium
* The price of a house, based on various data
* Survival statistics - i.e. the Titanic Kaggles problem
* Gender, based on height/weight

## Differences between Classification and Regression trees

### Regression

- used when the dependant variable is contineous (i.e. a numerical value, such as house price, waist width based on height/weight/gender), 
- the values at terminal nodes is variables is calculated based on the mean/average of the training data for the observations from the training data that end at the terminal node.

### Classification

* used when the dependant variable is categorical - i.e. gender, predicting  
* the values of terminal nodes is the mode of observations that end in that terminal node (the one that occurs most commonly)

## Visualisation

We are jumping ahead a little here, so we can have a visualisation of a tree. We are building a tree using `scikit-learn` trained on the [Titanic dataset from Kaggles](https://www.kaggle.com/c/titanic).

<script src="https://gist.github.com/readikus/1da220162fd9ab17e1ab04241bf07a5e.js"></script>

## The Algorithm - creating trees

* Decide what features to use?
* What conditions to split
* When to stop splitting
* Pruning

### Deciding where to split

* Split on all available features, and choose the split that results in the most homogeneous sub nodes. In this context, a homogeneous node is one where the values in it are closely related.

### Common algorithms

* Information gain
* Gini index - the degree of inequality in a distribution. Given a straight line through the data, the measure of difference with the elements.
* Chi squared
* Reduction invariance

Another visualisation of data plots like the video would be nice



Grow trees until
The splitting process
- put observations in a node, and split values until a user defined stopping criteria is reached - i.e. when each node has less than 50 training samples per node.

- but a fully grown tree, has a tendancy to overfit the data, so leads to low accuray on unseen data.
- pruning is used to handled over fitting.




# Example


# VISUALISATION...



Use Titanic dataset.

is male?

NO - survived
YES - is age over 9.5? -> DIED, else if siblings > 2.5 DIED, else SURVIVED




Carrot seeds

- early Nantes 2
salad leaves
french breakfast raddish   





