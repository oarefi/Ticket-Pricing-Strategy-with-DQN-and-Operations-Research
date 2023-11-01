# Ticket Pricing Strategy with DQN and Operations Research
## Overview
This repository contains Python code that employs both Deep Q-Network (DQN) and Operations Research (OR) methods to optimize ticket pricing strategies. The code provides an environment for simulating ticket sales, taking into account various parameters like days left for the event, tickets left, and current price.


## DQN Implementation Code Description
The DQN (Deep Q-Network) implementation is for a ticket pricing environment (TicketEnv) where the goal is to maximize the total reward earned from ticket sales over a 30-day period. The environment uses three main state variables: the number of days left (days_left), the number of tickets left (tickets_left), and the current price (price).

The DQNAgent class handles the learning process. It uses a neural network to approximate the Q-values for different actions and states. The model uses two hidden layers, each containing 24 neurons, and uses a mean squared error loss function for training.

act(): Decides which action to take based on the current policy (either exploring or exploiting).
remember(): Stores the experience in the memory.
replay(): Performs experience replay and trains the neural network.
The main loop runs for 500 episodes, each lasting 30 days, and the agent learns to act optimally in this environment. The rewards earned in each episode are plotted at the end.

## Average reward without OR: 8260.56

## DQN with OR (Operations Research) Implementation Code Description
The DQN with OR extends the basic DQN implementation by incorporating a linear programming objective (lp_objective) into the decision-making process. The agent optimizes both the immediate reward and a long-term objective related to operational metrics.

The function nested_optimization solves a linear program within the Q-Learning framework to compute the best action at each step. The objective is a weighted sum of the Q-value and the LP objective. This is integrated into the act() method of DQNAgent.

act(): Now uses nested_optimization to determine the action, thus balancing both immediate and long-term objectives.
Otherwise, the code structure remains similar to the basic DQN, including experience replay and epsilon decay. The key difference lies in the more nuanced action decision process.

## Average reward with OR: 8964.86

Both implementations use TensorFlow for neural network operations and Matplotlib for plotting the total rewards across episodes. The DQN with OR also uses the PuLP library for linear programming.
