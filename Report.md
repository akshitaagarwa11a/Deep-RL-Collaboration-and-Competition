# Report

## Implementation Details

I have used the Actor-Critic method, Deep Deterministic Policy Gradient model with multiple agents to solve the environment. Here 
the number of agents is 2.

## Model Description
I have used three fully-connected linear layers for both Actor and Critic networks. My first layer goes form the state size to 512, second layer form 512 to 256 and the third layer form 256 to action size. I have added batch normalization before each layer to make our model perform better. I have observed that in this environment both the agents are learning to do the same thing so it is like solving the Continuous robot arm environment with multiple agents. So I used a DDPG algorithm for two agents to solve this environment. It has worked pretty well. We could have used the MADDPG algorithm too but I think that it is suitable for a more complex task and this task is simple enough for DDPG to solve.</br>

***Hyperparameters***:
- BUFFER_SIZE = int(2e5) # replay buffer size
- BATCH_SIZE = 256       # minibatch size
- GAMMA = 0.99           # discount factor
- TAU = 2e-3             # for soft update of target parameters
- LR_ACTOR = 2e-4        # learning rate of the actor
- LR_CRITIC = 3e-3       # learning rate of the critic
- WEIGHT_DECAY = 0       # L2 weight decay

## Result
The environment was solved in 399 episodes with an average score of 0.51</br>
![Average score over 100 episodes](https://user-images.githubusercontent.com/31557923/69931684-2bedd400-14ee-11ea-8d61-06b4097e4c39.png)</br>
![Average score per episode](https://user-images.githubusercontent.com/31557923/69916923-e3e79680-1486-11ea-96ac-1b2a3d8a5304.png)

## Future Scope

MADDPG, PPO, A3C, D4PG can be applied to solve this environment. Moreover we can tune the hyperparameters further to solve the 
environment in lesser number of episodes.
