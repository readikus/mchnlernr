---
title: Random Forest 101
description: In this article we will look at the random forest algorithm and use it to make some predictions on house prices.
date: 2021-08-10
tags:
  - random forest
  - decision trees
  - algorithms
  - python
layout: layouts/post.njk
---

# Overview

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