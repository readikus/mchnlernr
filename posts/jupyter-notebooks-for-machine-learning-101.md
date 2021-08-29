---
title: Jupyter notebooks for machine learning
description: A look at using Jupyter notebooks for developing interactive Python
date: 2021-08-29
tags:
  - python
  - jupyter notebooks
  - tooling
layout: layouts/post.njk
---

## Overview

Jupyter notebooks offer an interactive way of creating Python code and detailed notes in a browser by combining REPLs and markdown. Whilst this approach doesn't scale for full applications, it is an excellent way to explore a dataset and understand the problems involved.

## Quick Start

The quickest way is to go over to the [Google Colaboratory](https://research.google.com/colaboratory) and have a play. You can create a series of cells containing markdown or Python.

## Running locally

By running locally, you are able to have full control on the version of Python you use and the available dependancies. The [Anaconda Navigator] introduced in the previous post, offers an easy way to run Jupyter notebooks locally.

## Jupyter Shortcuts

| Keys             | Command                             |
|------------------|-------------------------------------|
| shift + enter    | Run the current cell                |
| tab              | show popup of methods on an object  |
| shift + tab      | show the doc string for a function  |

## Sharing to gist

Gist are one of the easiest ways of making a Jupyter notebook shareable within a website (like this!). Colab has a nice feature to export notebooks direct to a gist in your GitHub account in the save menu. If you are developing locally, the following steps allow you to create a gist quickly:

1) Go to https://gist.github.com/YOUR-GITHUB-USERNAME/
2) Click 'New Gist' or `+` on the upper right corner
3) Drag and drop your local file and it should guide you through the rest.
4) Sharing is done from the gist, and it will have an "Embed" link near the top right.

And it will look something like this:

<script src="https://gist.github.com/readikus/b840218efb79158e681d97271edd1718.js"></script>