---
layout: post
title: Consensus-Based Inference and Control
date: 2022-12-10 00:00:00 +0300
description: projects
img: animation-flucking.gif # Add image post (optional)
tags: [Control, Distributed, Heuristic] # add tag
---
* This project solves a multi-agent control problem involving collision avoidance and tracking under uncertainty.

* Scenario: A group of smart devices (green dots) need to track an entity (yellow arrow) while coordinating to avoid collisions among themselves and with a moving threat (red dot).

* To avoid the moving threat and following the target, the devices compute consensus-based estimates of the threat and target’s positions using data collected locally (by its sensors) and via neighbor-to-neighbor communication.

* The devices use flocking to follow the target and avoid collisions. Flocking is a form of collective behavior that emerges from the local interactions of a large group of agents with a common objective.

### Take away

* Centralized approaches entail significant communication overhead and rely heavily on the performance of a single device (central node).

* Hierarchical communication strategies (devices share information using a tree structure) help, but the associated risk of relying too much on the central node remains.

* Linear consensus algorithms require minimal computation, communication, and synchronization to compute averages of local quantities (for example, estimates of a target’s position).

* Flocking is an efficient algorithm to compute collaborative control policies.

### Why it matters?

* Distributed methodologies like this one can help minimize the communication and computation consumption of devices forming Wireless Sensor Networks, a technology that is applicable in a wide range of monitoring applications (e.g., wildfire tracking, transportation surveillance, study of natural phenomena, etc.).

<br>
<br>
<hr />
Code available [here](https://github.com/ItzelOlivos/FinalProject677)