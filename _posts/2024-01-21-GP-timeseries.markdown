---
layout: post
title: Gaussian Process Regressor
date: 2024-01-21 13:32:20 +0300
description: projects
img: animation-spikes.gif # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [control, neuroscience]
---
* We develop a version of stochastic control that accounts for computational costs in the brain. 

* Combining concepts of efficient coding with control theory, we analyze Linear Quadratic Gaussian (LQG) control. LQG is a well-understood mathematical example of optimal control that combines a Kalman filter to keep track of a hidden state with a linear regulator that minimizes integrated quadratic state and action costs. When the state dynamics are linear, and all noise sources are Gaussian, this combination is your best bet!

* We assume the brain encodes uncertainty using a Probabilistic Population Code (PPC), which is a distributed neural representation that supports evidence integration through linear operations and marginalization through nonlinear operations

* We implement the Kalman filter using a spiking neural network:

    * Spike trains emitted by a sensory layer of neurons with Poisson-like response variability encode observations about the Gaussian world state. 
  
    * This neural response feeds a recurrent layer whose firing activity encodes the belief the agent would obtain by implementing recursive Bayesian estimation based on its last observation and action executed. 
  
    * The agent decodes the hidden world state using different projections of the neural activity emitted by the recurrent layer. 
  
    * The agent minimizes the expected total integrated state, action, and neural cost by adjusting its spike rates and control gain.

### Take away

* In this simplest version, the precision of the observation and inferences is directly proportional to the number of spikes. 

* We reveal a trade-off: an agent can obtain more utility overall by relinquishing some task performance if doing so saves enough spikes. 

* The optimal spike rate varies with the properties of the system to be controlled (for example, stability and signal-to-noise ratio).

### Why it matters?

* Previous efforts to identify metabolically efficient ways of coding sensory evidence are restricted to feedforward settings. Here, we consider the consequences of closed-loop control. 

* This work provides a foundation for a new type of bounded rational behavior that could be used to explain suboptimal computations in the brain.

* Understanding the mechanisms that give biological organisms an advantage over machines in perception and mobility can help engineer more robust, general-purpose, and energy-efficient robots.

<br>
<br>
<hr />
Tutorial available [here](https://github.com/ItzelOlivos/ItzelOlivos.github.io/blob/main/jp_tutorials/Gaussian_Processes.ipynb)