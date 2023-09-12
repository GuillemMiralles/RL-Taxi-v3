# Reinforcement Learning in OpenAI Gym: Tackling the Taxi Problem 🚖🤖

Introduction 🧐

This project delves into the Taxi problem within the OpenAI Gym environment, employing Reinforcement Learning techniques to tackle it. The Taxi problem sets a scenario where a virtual taxi driver must efficiently navigate a city to pick up passengers and transport them to their specified destinations. This dynamic environment presents challenges such as route planning, optimal decision-making, and time utilization optimization, all while adhering to traffic constraints and passenger demands.

Description of the Problem 🚖

The Taxi problem is unique in that the virtual driver must consider the passenger's current location, spatial limitations, and available pickup and drop-off locations. The driver's actions directly impact service quality and passenger satisfaction, adding an additional layer of optimization to the task.

Aims of the Work 🎯

The primary objective of this project is to apply and assess a Reinforcement Learning approach to address the challenging Taxi problem in the OpenAI Gym environment. The goal is to train an RL agent capable of learning an optimal policy to maximize efficiency in passenger pickup and drop-off, minimize travel time, and optimize routes. To achieve these goals, the project employs the Q-Learning algorithm, a well-known RL technique for learning optimal policies in discrete environments.

OpenAI Gym and Taxi-v3 Environment 🚕

The Taxi-v3 environment simulates a scenario where a taxi must pick up and drop off passengers at different locations in a city represented as a 5x5 grid. There are 500 discrete states, considering the taxi's location, passenger's location, pickup, and drop-off locations, and whether the passenger is inside the taxi. The taxi can take six actions, and rewards are assigned based on actions, with positive rewards for successful passenger delivery and negative rewards for incorrect actions.

Q-Learning 📚

Due to the Taxi problem's manageable size and full observability, the Q-Learning algorithm was chosen. Q-Learning is a reinforcement learning technique used to find an optimal policy in a Markov Decision Process (MDP). The core of Q-Learning is the Q-table, which records the expected "quality" of each action in each state.

The project also involves hyperparameter tuning using Hyperopt, a Bayesian optimization library. It defines a search space for key Q-Learning parameters like learning rate (alpha), discount rate (gamma), and exploration factor (epsilon). Hyperopt efficiently explores this parameter space to minimize the negative mean reward as the objective function.

Results: 🎯

The training results are analyzed, and a graph illustrates how total rewards change over episodes. Initially, the agent receives mostly negative rewards, indicating exploration and learning. As episodes progress, negative rewards decrease, reflecting the agent's improved decision-making. At 10,000 episodes, the taxi optimally solves the problem, consistently delivering passengers efficiently.

A video demonstrates the agent's learning process, showing its progress from erratic behavior to efficient task execution. Q-Learning proves effective in this scenario, consistently optimizing passenger pickup and delivery.

Conclusions: 📊

While Deep Reinforcement Learning (DRL) could have been considered for this task, Q-Learning proved to be a suitable and effective approach. It efficiently solved the Taxi problem over 10,000 training episodes, demonstrating the agent's ability to optimize its actions. The use of epsilon-greedy exploration and hyperparameter search ensured a well-balanced and effective learning process. Increasing the number of episodes may further improve performance.
