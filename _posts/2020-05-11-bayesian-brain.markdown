---
layout: post
title: Unraveling the mystery: How do humans reason so efficiently, and so quickly, in a world full of uncertainty?
date: 2020-05-11 00:00:00 +0300
description: myPosts
img: bayesian-brain.pdf
tags: [neuroscience] # add tag
---
In contrast to our current robots, that despite of being equipped with very precise sensors and 
sophisticated hardware, sitll struggle to operate under unexpected conditions, we possess the extraordinary ability
to reason efficiently in a world full of uncertainty. For instance, we can get up in the middle of the night, walk in the dim light, avoid
pointy furniture with our eyes almost completely closed, enter into the kitchen,
and enjoy a refreshing glass of water without a scratch. How is this possible?!

One way to shed light on the understanding of how and why are brains can handle uncertainty like a pro is to study how artificial agents 
solve sequential decision-making problems under uncertainty, 

To address uncertainty, artificial agents typically use a powerfull framework known as the "Partially Observable Markov Decision Process (POMDP)".
In this framework, the agent builds and maintains a posterior probability distribution over the hidden world state (for example, if I remember leaving marbles scattered on the floor, 
my brain needs to know exactly where they are to avoid tripping over them; however, since I don't want to disrupt my circadian rhythm, 
I shouldn't turn on the light, so the actual location of the marbles is a hidden variable that must be inferred based on the information I can barely see, hear, and remember). 
These probability distributions, known as "beliefs," are updated when new information arrives (for example, if I hear the marbles 
move when taking a step, my uncertainty about their position will decrease significantly) and are used to select actions that, 
based on all the sensory information acquired and inferred by the brain, maximize a reward function (that is, reaching the kitchen without a scratch).

For an artificial agent, solving 
1. Acquiring a model of how the environment evolves (e.g., what are the physical laws governing that small part of the universe directly related to the task of interest) 
2. Building beliefs about variables of interest.
3. Updating beliefs as the agent interacts with the environment, and 
4. Solving the optimization problem that determines the sequence of actions that maximizes the reward function. 

However, in the case of our brains, all the points described above must be implemented using only trains of electrical impulses
(known as spikes); these spikes are the mechanism by which neurons communicate almost instantaneously with each other and constitute 
one of the main differences in information processing between brains and computers.

Dr. Rao, in his research article "Decision-making under uncertainty: a neural model based on partially observable Markov decision process," 
published in the journal Frontiers in Computational Neuroscience, explains three reasons why it is plausible that the brain uses 
a mechanism similar to the algorithm that many artificial agents use today, Point-based POMDP:

The intrinsic noise of neuronal activity in the brain can encode probability distributions.
A circuit of neurons communicating recurrently can implement Bayesian inference (which allows us to draw conclusions from partial information).
Physiology studies demonstrate that the basal ganglia implements strategies similar to those of reinforcement learning-based agents to 
identify sequences of actions that maximize the reward function.

There is a long way to go before deciphering all the mysteries behind the mechanisms by which the brain can measure, 
manipulate, and reduce its uncertainty to decide how to behave rationally; however, this line of research offers 
interesting results that are well worth exploring.
