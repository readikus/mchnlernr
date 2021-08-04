---
title: Classification and Regression Trees (CART) 101
description: In this article we will look at the use of classification and regression trees for solving machine learning problems.
date: 2021-08-04
tags:
  - decision trees
layout: layouts/post.njk
---

# Overview

Classification and regression trees are like flow charts that allow us to reason about some input values and produce a classication or regression as a result.

Each node of the tree is a test on an attribute - for example, `age > 21` and each branch represents an outcome from the test. Terminal nodes represent the class labels - for example, if we were trying to detect spam emails, our nodes would be testing various factors, such as if certain words are included in the text, and the terminal nodes will tell us if we predict the email is spam or not spam.

In decision analysis, a decision tree can be used to visual represent the decisions being made. This is really important when we want to explain _why_ a machine learning algorithm made a particular classification.

# Advantages of CART

- Simple to understand, interpret and visualise
- Variable screening and feature selection
- Handles numerical as well as categorical data
- Minimal effort for data prepartion
- Non linear parameters do not affect the performance

# Disadvantages of CART

- Overfitting - over complex trees that do not generalise the data well.
- Variance - Pro to small variations in the data producing completely different trees. Handled by bagging and boosting.
- Greedy algorithms can not guarantee returning the optimal decision tree. Greedy algorithms make decisions that seem to be the best fit for that data, so it finds a local optimum rather than globally. See our [summary on random forest](./random-forest-101) for addressing this issue.
*-* Decision trees learners create biased trees. For example, predicting pauses in text-to-speech, most of the time we do not pause between words, so the data needs to be balanced to better represent the classes.

# Applications of Decision Trees





Random forests are an ensemble learning method for classification, regression and other tasks that operates by constructing a "forest" of decision trees at training time. For classification tasks, the output of the random forest is the class selected by most trees. For regression tasks, the mean or average prediction of the individual trees is returned.

## Pros:

- can perform both classification and regression.
- handles missing values and maintains accuracy
- not prone to overfitting
- handles large datasets with high dimensionality

## Cons

- good at classification, but not great at regression.
- very little control over what the model does

## Common Applications of Random Forest

- Banking: finding loyal customers/dodgy ones
- Medicine - validaing medicine, and identify disease by looking at medical records
- Stock market: stock behaviour, predicting likely loss or gain for a particular stock
- Ecommerce: likihood of a customer liking a particular product
- Computer vision: image classification. Xbox Connect uses random forest for classifying images of body parts    


# Algorithm Overview