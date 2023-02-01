# Reinforcement-learning
A course in reinforcement learning

## First problem: Taxi-v3
A simple CM implementation in OpenAI Gym's "Taxi-v3" environment. 

### What is OpenAI Gym?
[OpenAI Gym](https://gym.openai.com/) is a toolkit for developing and comparing reinforcement algorithms. It provides a wide range of environments with different reinforcement learning tasks.

### Task

We have 500 states and 6 actions. Using different strategies to maximize the total reward

### Parameters

We have 3 control parameters:
* n_sessions - sample this many sessions
* percentile - discard this percentage of sessions with lowest rewards
* learning_rate - how quickly the policy is updated, on a scale from 0 to 1

### Solve

1. Randomly select strategies, then select only the 'best strategies'. 

 _Init_:

![image](https://user-images.githubusercontent.com/84929000/215740783-4d94fec7-eafe-42f4-b082-8686c3029dc6.png)

 _Results_:

![image](https://user-images.githubusercontent.com/84929000/215740884-0884513e-f51c-41bc-81ad-00fab3aeec3c.png)

2. 


