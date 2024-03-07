---
layout: post
title: Harnessing the power of AI to reveal the secrets of the most powerful reasoning engine ever designed
date: 2023-11-07 00:00:00 +0300
description: myPosts
img: bayesian-brain.pdf
tags: [neuroscience] # add tag
---
In contrast to our current robots, who, despite being equipped with very precise sensors and sophisticated hardware, still struggle to operate under unexpected conditions, we (humans) possess the extraordinary ability to reason efficiently in a world full of uncertainty. For instance, we can get up in the middle of the night, walk in the dim light, avoid
pointy furniture with our eyes almost closed, enter the kitchen,
and enjoy a refreshing glass of water. How is this possible?!

One way to shed light on the mechanisms that allow our brain to handle uncertainty like a pro is to study how brain-like constrained artificial agents solve sequential decision-making problems under uncertainty. 

The Partially Observable Markov Decision Process (POMDP) is a powerful framework that allows artificial agents to reason amidst uncertainty. In this framework, the agent builds and maintains a posterior probability distribution over the hidden world state (for example, if I remember leaving marbles scattered on the floor, 
my brain needs to know where they are to avoid tripping over them; however, since I don't want to disrupt my circadian rhythm, 
I cannot turn on the light, so the actual location of the marbles is a hidden variable that must be inferred based on the information I can barely see, hear, and remember). This probability distribution, known as "belief," is updated when new information arrives (for example, if I hear the marbles move when taking a step, my uncertainty about their position will decrease significantly). The agent uses the evolving belief to select the sequence of actions that maximizes expected cumulative reward and reaches the goal: reaching the kitchen without a scratch!

Solving a POMDP, in its most general form, is an exciting challenge that requires addressing hard computational problems:
Learning: Using experience to fit a cognitive map (a.k.a. model) that explains how the environment evolves. This model enables the generation of new data for further training, allows making predictions that improve transfer learning and generalization to novel environments, and simplifies explaining and interpreting the agent's behavior.
Inferring: Updating the belief over the hidden world state as the agent interacts with the environment. The belief allows the agent to be aware of the world's uncertainty, quantify it, take actions to reduce it, draw conclusions about the current world state based on partial information, and predict expected future rewards.
Planning: Solving the optimization problem that determines the sequence of actions that maximizes the expected cumulative reward.

Learning, Inferring, and planning are resource-intensive processes. Our current artificial agents rely on the availability of virtually unlimited resources (time, memory, and computing power) to produce approximate solutions. Below, you can find state-of-the-art approaches to solving POMDPs and representative papers where you can learn more about them:
* Model the environment as if it were fully observable. Keep track of the epistemic uncertainty introduced by the mismatched world model. Solve the planning problem, taking into account the effects of epistemic uncertainty. 
  * [Deep Reinforcement Learning in a Handful of Trials using Probabilistic Dynamics Models](https://proceedings.neurips.cc/paper_files/paper/2018/file/3de568f8597b94bda53149c7d7f5958c-Paper.pdf)
  * [Gaussian Processes for Data-Efficient Learning in Robotics and Control](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6654139)
* Learn a generative model (which is a cognitive map that explains transitions between states and how these states produce new observations). Use the model as a feedforward predictor. Implement a Model Predictive Controller that maximizes expected cumulative reward as if the predictions were the actual states of the world. 
  * [World Models](https://arxiv.org/pdf/1803.10122.pdf)
  * [Graph Networks as Learnable Physics Engines for Inference and Control](http://proceedings.mlr.press/v80/sanchez-gonzalez18a/sanchez-gonzalez18a.pdf)
* Learn a generative model. Use the model to build and maintain an evolving belief over the hidden world state. Find the policy (a mapping from beliefs to actions) that jointly optimizes the accuracy of the model and the expected utility. 
  * [Deep Variational Reinforcement Learning for POMDPs](http://proceedings.mlr.press/v80/igl18a/igl18a.pdf)
  * [Discriminative Particle Filter Reinforcement Learning for Complex Partial Observations](https://arxiv.org/pdf/2002.09884.pdf)
* Learn a generative model. Use it to express the joint probability distribution of the sequence of states, actions, and observations. Solve the problem via Control as Inference. 
  * [Stochastic Latent Actor-Critic: Deep Reinforcement Learning with a Latent Variable Model](https://proceedings.neurips.cc/paper/2020/file/08058bf500242562c0d031ff830ad094-Paper.pdf)

It's impressive that, while today's machines struggle to develop control strategies robust to uncertainty, living organisms have already resolved this issue through millions of years of evolution! Picture, for example, the spectacular precision of a peregrine falcon as it finds prey and estimates the trajectory of its deadly, high-speed dive or the graceful agility of a hummingbird avoiding collisions as it traverses dense foliage in search of nectar-filled flowers.

Behavioral experiments consistently show that brains use 
mechanism similar to those used by artificial agents when solving control tasks. It is also widely accepted that brains engage in probabilistic inference to reason under uncertainty! However, brains and machines process information in entirely different ways. To represent and process information, the brain uses trains of electrical impulses (spikes) that consume a significant fraction of its total energy. This representational constraint diminishes our ability to draw accurate conclusions and forces us to accept trade-offs: our brain can obtain more utility overall by relinquishing some task performance if doing so saves enough spikes.

As a Ph.D. student, I've delved deep into unraveling the brain's mastery in tackling joint inference and control problems with resource efficiency. By studying how brain-like constrained artificial agents solve hard control problems using partial observations, we can gain insights to design more robust and power-efficient machines. This is crucial to allowing resource-constrained devices like drones, nanobots, and AI-powered prosthetics to thrive in real-world settings. 

Do you want to learn more about the synergy between brains, minds, and machines? Check this out:

[Control when confidence is costly]()
[Spike-Constrained Stochastic Control](https://itzelolivos.github.io/spike-lqg/)
[Engineering a Less Artificial Intelligence](https://www.cell.com/neuron/pdf/S0896-6273(19)30740-8.pdf)
[Computational rationality: A converging paradigm for intelligence in brains, minds, and machines](https://www.science.org/doi/pdf/10.1126/science.aac6076?casa_token=G_kpCItA7jkAAAAA:fRAYrnqu_XHRgpIJkI9QX9xx55ZyJtl7YajNx9qfk1ShHQF0oO_o6SZNaaOqekyBbukceS3xImanTA)
[Building Machines That Learn and Think Like People](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/A9535B1D745A0377E16C590E14B94993/S0140525X16001837a.pdf/building-machines-that-learn-and-think-like-people.pdf)
