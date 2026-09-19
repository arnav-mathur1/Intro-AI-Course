# Intro to AI Course

In this repo, I'll discuss some of the projects/assignments I was able to work on through the 07-180 Concepts of AI course at CMU. Spring 2025

# Project 1: Search & Rescue with Classical Search

Built a search-and-rescue planning system for navigating a damaged building represented as a grid.

The environment included walls, victims, an entry point, and cells with different obstruction costs. Depending on the task, we had to either reach a victim or retrieve one and return to the entry point.

I worked on:
- the core frontier/explored-set search algorithm
- path-cost and heuristic calculations
- Uniform Cost Search, Greedy Search, and A* priority functions
- Search & Rescue state transitions and action costs
- Manhattan-distance and cost-to-go heuristics

The same search framework supported DFS, BFS, UCS, Greedy Search, and A*. The generated plan was then executed in a graphical simulator.

# Project 2: Traffic Control with Markov Decision Processes

Modeled a stochastic traffic intersection as a Markov Decision Process.

Cars arrive and leave probabilistically, and we must decide how to operate the traffic lights while minimizing long-term costs such as waiting time, light changes, and collisions.

I implemented:
- expected value calculations over stochastic transitions
- Bellman updates
- value iteration
- best-action selection and policy extraction
- traffic state generation
- probabilistic arrival and departure transitions
- reward and cost modeling

The resulting policy was executed in a traffic simulator where the intersection evolved stochastically over time.

# Project 3: Reinforcement Learning for Search & Rescue

This assignment implemented a Q-learning agent and applied it to the Search & Rescue environment.

Unlike the classical search project, the RL agent did not plan using the full known map. Instead, it learned from repeated interaction with the environment using local observations and rewards.

I implemented:
- the Q-learning update rule
- greedy action selection
- epsilon-greedy exploration
- visitation-based learning rates
- UCB-style exploration for the Search & Rescue agent

The agent observed a local 5x5 view of the environment and learned a navigation policy through repeated training trials.

# Project 4: Decision Trees + Neural Networks

This assignment extended the Search & Rescue environment with ML so the agent had to make decisions using predicted information rather than a perfectly known map.

The system used a decision tree to predict obstruction costs for map cells and a neural network to determine whether possible victim locations contained real victims.

I implemented:
- entropy and information gain
- recursive decision tree construction
- decision tree pruning
- fully connected neural network forward propagation
- N-fold cross-validation for neural network training
- training and application of obstacle-cost and victim classifiers

The resulting predictions were used to construct the agent's believed map, which was then passed to A* for planning. The same decision tree and neural network implementations were also applied to handwritten-digit classification using a subset of MNIST.

# Demos

I have uploaded videos of demos to the first two projects to this repo.
