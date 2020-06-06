# Deep RL Banana Navigator
We train an agent to manuver in a 3-D environment avoiding blue bananas and picking yellow ones as fast as possible. We do this by implementing Deep Q network based on this research paper. The agent works thorugh Agent class in dqn_agent.py and the model architecture is described in model.py.

I have described my approach and the code in a more detailed manner in Report.pdf

[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

# Project 1: Navigation

### Environment
!["GIF"](https://github.com/ShivankYadav/BananaPicker-Navigation/blob/master/images/banana.gif)

A **reward** of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.


### Rewards

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

### States and Actions

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

### Files in this Repository
                    
    .
    ├── checkpoint.pth                     # latest stored weights for trained neural network
    ├── dqn_agent.py                       # agent to interact and learn from environment
    ├── model.py                           # neural network model (in Pytorch)
    ├── Navigation.ipynb                   # main code for training and testing the agent
    ├── Report.pdf                         # report of the implementation and details of the learning algorithm
    ├── tr_checkpoint_1000it_64_64.pth     # stored weights of trained network (1000 iterations, 2 hidden 64 unit layers)
    └── README.md

### Python Packages
 - gym
 - random
 - torch
 - numpy
 - collections
 - matplotlib
 - unityagents
 
**Note:** The Unity environment did not work on Mac OS for Python version 3.7 and higher. Python version 3.6 worked well.


### Downloading the Environment

You need only select the environment that matches your operating system:
 - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
 - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
 - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
 - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Place the application in the same directory before executing.

(_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.




