# Project: Navigation

# Introduction

In this project the agent is navigating in a large square world with a purpose, collecting bananas! The agent gets a reward of +1 each time it gets a yellow banana and -1 if it gets a blue one. So the goal is for the agent to collect as many yellow bananas and to avoid as many blue bananas as possible. The state space has 37 dimensions which contains agent's velocity, as well as perception of objects around its forward direction. The agent is able to take four discrete actions:

- 0 - move forward
- 1 - move backward
- 2 - turn left
- 3 - turn right

The environment is considered solved if the agent can get an average score of +13 over 100 consecutive episodes.

# Learning Algorithm

The agent uses DQN for it's perception (analysis) and decisioning. 

## Architecture

```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Linear-1                   [-1, 64]           2,432
              ReLU-2                   [-1, 64]               0
            Linear-3                   [-1, 64]           4,160
              ReLU-4                   [-1, 64]               0
            Linear-5                    [-1, 4]             260
================================================================
Total params: 6,852
Trainable params: 6,852
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.00
Params size (MB): 0.03
Estimated Total Size (MB): 0.03
----------------------------------------------------------------
```

## Hyperparameters

```python
BUFFER_SIZE = int(1e5)  # replay buffer size
BATCH_SIZE = 64         # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR = 5e-4               # learning rate 
UPDATE_EVERY = 4        # how often to update the network
```

# Performance

The agent first achieved the target score episode 249 and converged at around episode 600.

![Project%20Navigation%20bc875a7696184568982d10f11c058563/Screen_Shot_2021-02-17_at_9.10.38_PM.png](Project%20Navigation%20bc875a7696184568982d10f11c058563/Screen_Shot_2021-02-17_at_9.10.38_PM.png)

The agent is able to receive an average reward (over 100 episodes) of +15.5

![Project%20Navigation%20bc875a7696184568982d10f11c058563/Screen_Shot_2021-02-17_at_9.46.46_PM.png](Project%20Navigation%20bc875a7696184568982d10f11c058563/Screen_Shot_2021-02-17_at_9.46.46_PM.png)

# Install & Run

To install the requirements, use `pip install -r requirements.txt`

To run the code, simply run the `Navigation.ipynb` notebook, cell by cell.