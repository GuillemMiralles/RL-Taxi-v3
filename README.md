<!DOCTYPE html>
<html>
<head>
  <title> Reinforcement Learning in OpenAI Gym: Tackling the Taxi Problem 🚖🤖 </title>
</head>
<body>
  <h1>Introduction 🧐</h1>
  <p>This project delves into the Taxi problem within the OpenAI Gym environment, employing Reinforcement Learning techniques to tackle it. The Taxi problem sets a scenario where a virtual taxi driver must efficiently navigate a city to pick up passengers and transport them to their specified destinations. This dynamic environment presents challenges such as route planning, optimal decision-making, and time utilization optimization, all while adhering to traffic constraints and passenger demands.</p>

  <h2>Description of the Problem 🚖</h2>
  <p>The Taxi problem is unique in that the virtual driver must consider the passenger's current location, spatial limitations, and available pickup and drop-off locations. The driver's actions directly impact service quality and passenger satisfaction, adding an additional layer of optimization to the task.</p>

  <h2>Aims of the Work 🎯</h2>
  <p>The primary objective of this project is to apply and assess a Reinforcement Learning approach to address the challenging Taxi problem in the OpenAI Gym environment. The goal is to train an RL agent capable of learning an optimal policy to maximize efficiency in passenger pickup and drop-off, minimize travel time, and optimize routes. To achieve these goals, the project employs the Q-Learning algorithm, a well-known RL technique for learning optimal policies in discrete environments.</p>

  <h2>OpenAI Gym and Taxi-v3 Environment 🚕</h2>
  <p>The Taxi-v3 environment simulates a scenario where a taxi must pick up and drop off passengers at different locations in a city represented as a 5x5 grid. There are 500 discrete states, considering the taxi's location, passenger's location, pickup, and drop-off locations, and whether the passenger is inside the taxi. The taxi can take six actions, and rewards are assigned based on actions, with positive rewards for successful passenger delivery and negative rewards for incorrect actions.</p>

  <h2>Q-Learning 📚</h2>
  <p>Due to the Taxi problem's manageable size and full observability, the Q-Learning algorithm was chosen. Q-Learning is a reinforcement learning technique used to find an optimal policy in a Markov Decision Process (MDP). The core of Q-Learning is the Q-table, which records the expected "quality" of each action in each state.</p>
  <p>The project also involves hyperparameter tuning using Hyperopt, a Bayesian optimization library. It defines a search space for key Q-Learning parameters like learning rate (alpha), discount rate (gamma), and exploration factor (epsilon). Hyperopt efficiently explores this parameter space to minimize the negative mean reward as the objective function.</p>

  <h2>Results: 🎯</h2>
  <p>The training results are analyzed, and a graph illustrates how total rewards change over episodes. Initially, the agent receives mostly negative rewards, indicating exploration and learning. As episodes progress, negative rewards decrease, reflecting the agent's improved decision-making. At 10,000 episodes, the taxi optimally solves the problem, consistently delivering passengers efficiently.</p>
  <p>A video demonstrates the agent's learning process, showing its progress from erratic behavior to efficient task execution. Q-Learning proves effective in this scenario, consistently optimizing passenger pickup and delivery.</p>

  <h2>Conclusions: 📊</h2>
  <p>While Deep Reinforcement Learning (DRL) could have been considered for this task, Q-Learning proved to be a suitable and effective approach. It efficiently solved the Taxi problem over 10,000 training episodes, demonstrating the agent's ability to optimize its actions. The use of epsilon-greedy exploration and hyperparameter search ensured a well-balanced and effective learning process. Increasing the number of episodes may further improve performance.</p>

  <h2>📂 Files</h2>
  <ul>
    <li><a href="Taxi_RL.ipynb">Taxi_RL.ipynb</a>: Full code of this project.</li>
    <li><a href="Training_video.mp4">Training_video.mp4</a>: The video that demonstrates the agent's learning process</li>
  </ul>

  
</body>
</html>

