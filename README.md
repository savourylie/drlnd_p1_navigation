# README

# Introduction

In this project the agent is navigating in a large square world with a purpose, collecting bananas! The agent gets a reward of +1 each time it gets a yellow banana and -1 if it gets a blue one. So the goal is for the agent to collect as many yellow bananas and to avoid as many blue bananas as possible. The state space has 37 dimensions which contains agent's velocity, as well as perception of objects around its forward direction. The agent is able to take four discrete actions:

- 0 - move forward
- 1 - move backward
- 2 - turn left
- 3 - turn right

The environment is considered solved if the agent can get an average score of +13 over 100 consecutive episodes.

# Installation

## Python and packages

To install the python requirements, use `pip install -r requirements.txt`.

## Project environment

The project environment can be downloaded from [here](https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation#getting-started).

# Run

To run the code, simply run the `Navigation.ipynb` notebook, cell by cell.