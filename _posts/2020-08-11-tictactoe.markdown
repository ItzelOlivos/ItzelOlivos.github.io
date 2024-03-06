---
layout: post
title: Q-learning Masters Tic Tac Toe
date: 2020-08-11 00:00:00 +0300
description: projects
img: animation-tictactoe.gif # Add image post (optional)
tags: [Programming, Learn] # add tag
---
* This project uses Q-learning to allow an artificial agent to play Tic Tac Toe.

### Take away

* Q-learning is a model-free Reinforcement Learning (RL) algorithm: The agent interacts with the environment to devise a mapping from states to actions that maximize the expected cumulative reward the agent receives over time.

* The learning process starts with a randomly initialized Q-table that encodes the "value" of taking a particular action in a given state; as the agent interacts with the environment, it updates the table using the [Bellman equation](https://en.wikipedia.org/wiki/Bellman_equation) until convergence.

* The Bellman equation is the essential ingredient of Dynamic Programming. This optimization method breaks down the computational complexity of planning.

* Once the values of the Q-table converge, the agent has access to a lookup table that matches (state, action)-pairs with its associated "quality." In the context of RL, the quality of the pair (S, A) represents how useful it would be, in the quest to reach the goal, to take action A when the agent reaches state S.

* The lookup table allows the agent to be greedy! Choosing an action at each time step is now as simple as finding the current state in the rows and selecting the action with the highest quality in the columns.

* To master Tic Tac Toe, the agent builds a Q-table that has 3^9 rows (This accounts for all possible scenarios given that the boardgame has 9 cells, and each one can be either empty, contain an X, or contain an O) and 9 columns (during its turn, the agent can select an available cell, out of 9, to write its mark)

### Why it matters?

* Q-learning is straightforward to implement and works very well when the state and action spaces are discrete (and relatively small).

* Q-learning can be combined with Deep Neural Networks to solve more complex challenges involving continuous state spaces. Instead of encoding the Q-values using a table, we can encode them using a deep 
<br>
<br>
<hr />

To train the agent or to play against an agent already trained, click [here](https://github.com/ItzelOlivos/TicTacToe)