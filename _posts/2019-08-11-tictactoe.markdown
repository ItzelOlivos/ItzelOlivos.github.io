---
layout: post
title: Q-learning Masters Tic Tac Toe
date: 2019-08-11 00:00:00 +0300
description: projects
img: animation-tictactoe.gif # Add image post (optional)
tags: [Programming, Learn] # add tag
---
### What is it about?

* This project uses Q-learning to allow an artificial agent to play Tic Tac Toe.

### Take away

* Q-learning is an off-policy reinforcement learning algorithm (RL): The agent interacts with the environment to devise an approximately optimal policy. Upon convergence, the agent uses this policy to maximize the expected cumulative reward during future interactions with the environment.

* The learning process starts with a randomly-initialized matrix, then the agent interacts with the environment and updates the table using the Bellman equation. The process stops once the q-table has converged.

* Once trained, the agent will have access to a lookup table that matches (state, action)-pairs with its associated "quality." In the context of RL, the quality of the pair (S, A) represents how useful it would be, in the quest to reach the goal, to take action A when the agent touches state S.

* The lookup table allows the agent to be greedy! Choosing an action at each time step is now as simple as finding the current state in the rows and selecting the action in the columns with the highest quality.

* To master Tic Tac Toe, the agent's builds a Q-table that has 3^9 rows (This accounts for all possible scenarios given that the boardgame has 9 cells, and each one can be empty, contain an X, or contain an O) and 9 columns (during its turn, the agent can select an available cell, out of 9, to write its mark)

### Why it matters?

* Q-learning is straightforward to implement and works very well when the state and action spaces are discrete (and relatively small)!
<br>
<br>
<hr />

To train the agent or to play against an agent already trained, click [here](https://github.com/ItzelOlivos/TicTacToe)