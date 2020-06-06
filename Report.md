# Banana Navigator with Deep Reinforcement Learning

To solve the first project of the Udacity Reinforcement Learning Nanodegree, a Deep Q-Network with the details in this report was used to let an agent navigate in an Unity environment.

## 1. The Enviroment

The agent to train navigates in an Unity environment consisting of a large square world with the goal to collect as many yellow bananas as possible whilst avoiding the blue bananas.

## 1.1 States and Actions

The state space consists of 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select action.

The four discrete actions available to the agent are:
* 0 - move forward
* 1 - move backward
* 2 - turn left
* 3 - turn right

The task is episodic and is solved when the agent reaches a score of +13 over 100 consecutive eposieds.

## 2.1 Network Architecture

The model, used to solve the environment, has two fully connected hidden layers with 64 units each.

So to summarize the layer structure(in model.py)

**37 units(input)  - 64 units (1st hidden) - 64 units (2nd hidden) - 4 units (output)**

2.2 Network Hyper-parameters

Folloing hyper-parameters were used for training:


| Parameter               | Value |
| ----------------------- | ----- |
| Buffer size             | 1e5   |
| Batch size              | 64    |
| Gamma (discount factor) | 0.99  |
| tau(soft update interpolation) | 1e-3 |
| learning rate| 5e-4|
| update rate| 4 |
| episodes| 1000|
| max timestamps per episode | 1000|
| epsilon start | 1.0|
| epsilon end|  0.01|
| epsilon decay| 0.95|

## 3 Training Results

The rewards over the number of episodes can be found below. Notice that the envrionment was solved around 400 episodes (solved means a score of +13 over 100 consecutive episodes). However for the sake of performance improvement, the agent was trained until 1000 episodes, which led to signifficant improvements.

## 4 Ideas for Future Work

Another approach to tackle this problem would be learning directly from the pixels of the envrionment. This would need some convolutional layers as described in the initial paper of DQN.
More over, it is important aspect to further tune the hyper-parameters to reach better performance.
Once could also aim for improved performance by using optimized variants of Deep Q-Networkds( for example, Dueling-DQN, Double-DQN...)

