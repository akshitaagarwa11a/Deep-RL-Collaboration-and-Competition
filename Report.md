# Report

## Implementation Details

I have used the Actor-Critic method, Deep Deterministic Policy Gradient model with multiple agents to solve the environment. Here 
the number of agents is 2.

## Model Description
I have used three fully-connected linear layers for both Actor and Critic networks.</br>

***Hyperparameters***:
- BUFFER_SIZE = int(2e5) # replay buffer size
- BATCH_SIZE = 256       # minibatch size
- GAMMA = 0.99           # discount factor
- TAU = 2e-3             # for soft update of target parameters
- LR_ACTOR = 2e-4        # learning rate of the actor
- LR_CRITIC = 3e-3       # learning rate of the critic
- WEIGHT_DECAY = 0       # L2 weight decay

## Result
The environment was solved in 371 episodes with an average score of 0.51

## Future Scope

MADDPG, PPO, A3C, D4PG can be applied to solve this environment. Moreover we can tune the hyperparameters further to solve the 
environment in lesser number of episodes.
