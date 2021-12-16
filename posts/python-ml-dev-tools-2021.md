---
title: Machine Learning development with Python in 2021
description: In this article we will give an opinonated overview of what tools help with developing model-independent Python in 2021.
date: 2021-10-01
tags:
  - python
  - package management
  - tooling
layout: layouts/post.njk
---

Coming from a JavaScript-based team, that employ a number of node contributors, I had easy access to the latest best practice, and the tools made development life great. Switching to Python, I didn't have the luxury of access to experienced developers who were able to point me at the right tooling. But I do have Google and spare time to learn.

I started a course recently in data visualisation, so was taking a steer from a lot of the recommendations in there. But when I went back to doing a little bit of work on one of my open source Python packages, I hit a number of snags that cost me hours to fix/sidestep.

In this summary (which I will keep updated as I learn more) I have included the tooling I use for IDE-based python development 

# Package management

Poetry! Almost as good as NPM, and makes it easy. Not only does it handle virtual environments and dependancy versions, it allows you to create custom scripts (I've added a test script `poetry run test` that runs all my unit tests automatically).

# Git Helpers

I will come back later to pre commit hooks...

# Linting

Black!!! It's extremely opinonated, and you have to just go with it. The assumption being if everyone else does, it removes any stylisitic discussions/disagreements/fights during PRs. The only thing that seems configurable is line length, which is important getting black to run along side other static code tools.

# Static code analysis

# Unit testing

# Putting it together




# Google Colab


# Things to avoid:

Anaconda - just a bit bulky

I have been spoilt working commercially in the JavaScript world by the `npm` package manager and it's related eco-system. When I have been working with python, there are numerous frustrations related to versioning and working with third party packages. It is these third party packages that have made Python _the_ programming language for machine learning.</p>

### Why?

Anaconda is an open source toolkit for:

* Dependancy management - provides a cloud-based repository of over 7,500 data science and machine learning packages.
* Manage Environments - makes it easy to manage multiple environments that can be maintained and run separately without interference from each other.

### Why can't I just use `pip`, `easy_install` and `virtualenv`/`pyenv`?

Good question! The simple answer is that `Conda` support dependancies that sit outside the Python ecosystem. This [Conda blog post](http://web.archive.org/web/20170415041123/www.continuum.io/blog/developer-blog/python-packages-and-environments-conda) addresses this question:

> Having been involved in the python world for so long, we are all aware of `pip`, `easy_install`, and `virtualenv`, but these tools did not meet all of our specific requirements. The main problem is that they are focused around Python, neglecting non-Python library dependencies, such as HDF5, MKL, LLVM, etc., which do not have a setup.py in their source code and also do not install files into Python’s site-packages directory.

What are these libraries that get mentioned?

* [HDF5](https://www.hdfgroup.org/solutions/hdf5/): HDF5 is a unique technology suite that makes possible the management of extremely large and complex data collections.
* [MKL](https://software.intel.com/content/www/us/en/develop/tools/oneapi/components/onemkl.html): Developed specifically for science, engineering, and financial computations, Intel™ Math Kernel Library (MKL) is a set of threaded and vectorized math routines that work to accelerate various math functions and applications.
* [LLVM](https://llvm.org/docs/GettingStarted.html): The LLVM Project is a collection of modular and reusable compiler and toolchain technologies. 

### Installation

[The Anaconda site](https://anaconda.cloud/tutorials/getting-started-with-anaconda-individual-edition
) will do a much better job of this than I can. Saying that, my first installation failed, and I had to `rm` the files and start again (the docs show the old location, it's now `rm -rf ~/opt/anaconda3`). 

### Anaconda Navigator

Introduced above, this provides a nice visual UI for running a set of tools, and managing dependancies. From the main window, you can launch a Jupyter notebook and start coding.

You're now well set for building notebooks locally.