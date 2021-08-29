---
title: Getting Started with Anaconda Python distribution for Machine Learning
description: In this article we will give a quick overview of Anaconda for various code management tasks.
date: 2021-08-29
tags:
  - python
  - package management
  - tooling
layout: layouts/post.njk
---

## Overview

I have been spoilt working commercially in the JavaScript world by the `npm` package manager and it's related eco-system. When I have been working with python, there are numerous frustrations related to versioning and working with third party packages. It is these third party packages that have made Python _the_ programming language for machine learning.

## Why?

Anaconda is an open source toolkit for:

* Dependancy management - provides a cloud-based repository of over 7,500 data science and machine learning packages.
* Manage Environments - makes it easy to manage multiple environments that can be maintained and run separately without interference from each other.

## Why can't I just use `pip`, `easy_install` and `virtualenv`/`pyenv`?

Good question! The simple answer is that `Conda` support dependancies that sit outside the Python ecosystem. This [Conda blog post](http://web.archive.org/web/20170415041123/www.continuum.io/blog/developer-blog/python-packages-and-environments-conda) addresses this question:

> Having been involved in the python world for so long, we are all aware of `pip`, `easy_install`, and `virtualenv`, but these tools did not meet all of our specific requirements. The main problem is that they are focused around Python, neglecting non-Python library dependencies, such as HDF5, MKL, LLVM, etc., which do not have a setup.py in their source code and also do not install files into Python’s site-packages directory.

What are these libraries that get mentioned?

* [HDF5](https://www.hdfgroup.org/solutions/hdf5/): HDF5 is a unique technology suite that makes possible the management of extremely large and complex data collections.
* [MKL](https://software.intel.com/content/www/us/en/develop/tools/oneapi/components/onemkl.html): Developed specifically for science, engineering, and financial computations, Intel™ Math Kernel Library (MKL) is a set of threaded and vectorized math routines that work to accelerate various math functions and applications.
* [LLVM](https://llvm.org/docs/GettingStarted.html): The LLVM Project is a collection of modular and reusable compiler and toolchain technologies. 

## Installation

[The Anaconda site](https://anaconda.cloud/tutorials/getting-started-with-anaconda-individual-edition
) will do a much better job of this than I can. Saying that, my first installation failed, and I had to `rm` the files and start again (the docs show the old location, it's now `rm -rf ~/opt/anaconda3`). 

## Anaconda Navigator

Introduced above, this provides a nice visual UI for running a set of tools, and managing dependancies. From the main window, you can launch a Jupyter notebook and start coding.

You're now well set for building notebooks locally.