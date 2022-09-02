---
layout: post
title: Consensus-Based Inference and Control
date: 2021-12-10 00:00:00 +0300
description: projects
img: animation-flucking.gif # Add image post (optional)
tags: [Control, Distributed, Heuristic] # add tag
---
### What is it about?

* This project solves a multi-agent control problem involving collision avoidance and tracking under uncertainty.

* Scenario: A group of smart devices (green dots) need to track an entity (yellow arrow) while coordinating to avoid collisions among themselves and with a moving threat (red dot). 

* To avoid the moving threat and following the target, the devices compute consensus-based estimates of the threat and target's positions using data collected locally (by its own sensors) and via neighbor-to-neighbor communication.

* To follow the target and avoid collisions, the devices use Flocking. This is a form of collective behavior that emerges from local interactions of a large group of agents with a common objective. 

### Take away

* Centralized approaches entail significant communication overheard and rely heavily on the performance of a single device (central node). 

* Hierarchical communication strategies (devices share information using a tree structure) help, but the associated risk of relying too much on the central node remains. 

* Linear consensus algorithms require minimal computation, communication, and synchronization to compute averages of local quantities (for example, estimates of a target's position).

* Flocking is an efficient algorithm to compute collaborative control policies.

### Why it matters?

* Distributed methodologies like this one can help minimize the communication and computation consumption of devices forming Wireless Sensor Networks, a technology with applicability in a wide number of monitoring applications (wildfire tracking, transportation surveillance, study of natural phenomena, etc.) 

<br>
<br>
<hr />
Code: [Repo](https://github.com/ItzelOlivos?tab=repositories)