---
layout: post
title: Gaussian Process Regressor
date: 2023-08-15 13:32:20 +0300
description: projects
img: animation-spikes.gif # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [timeseries, machine learning]
---
### Gaussian Process (GP)

A GP is a Gaussian distribution over functions. Example: f is a GP if f(x) = [f(x1), f(x2),..., f(xn)] is Gaussian distributed for any vector [x1, x2, ..., xn]

A GP is specified by a mean [mu(x1), ..., mu(xn)] and a covariance/kernel function K_{i, j} = k(xi, xj)

Given a set of observed inputs, corresponding output values, and a Gaussian process prior, we can compute the posterior over the value f(x) at any query input x. How?

Find the joint distribution [f(x*), f(x1), ..., f(xn)]

Use the conditioning rules for a Gaussian to compute f(x*) | f(x1), ..., f(xn)

GPs can handle noise versions of input values because [f(x*), f(y1), ..., f(yn)] with yi = xi + (white Gaussian noise) is also Gaussian

The kernel parameters (length scale and noise variance) are chosen such that they maximize the log likelihood of the observed data (Don't forget to cross-validate!)

Computational complextity:

O(N^3) computations to find the posterior mean weight vector and O(N c) to make a prediction, with N:=number of observations and c:=complexity of evaluating the kernel.
GPs scale badly, however, a linear kernel (aka Bayesian Linear Regression) can help: O(d^3) computations needed to find the posterior mean weight vector and O(d) to make predictions, with d:=dimension of the input

### Take away

* mmm

### Why it matters?

* mmm

<br>
<br>
<hr />
Tutorial available [here](https://github.com/ItzelOlivos/ItzelOlivos.github.io/blob/main/jp_tutorials/Gaussian_Processes.ipynb)