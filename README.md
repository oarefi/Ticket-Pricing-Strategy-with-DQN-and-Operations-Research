# Ticket Pricing Strategy with DQN and Operations Research

## Overview

This repository contains Python code that employs a robust, simulation-based framework using both Deep Q-Network (DQN) and Operations Research (OR) methods to optimize ticket pricing strategies. The code is designed to function in an environment simulating ticket sales for events, taking into account various parameters like days left for the event, tickets left, and the current price. While initially targeted at ticket sales, this system's methodologies can be applied across various domains like finance, e-commerce, and healthcare, thereby demonstrating versatility in tackling complex, multi-dimensional challenges.

## DQN Implementation Code Description
The DQN implementation operates in a ticket pricing environment (TicketEnv) where the objective is to maximize the total revenue earned, denoted as the average reward, from ticket sales over a 30-day period.

## Key Functionalities:
act(): Decides which action to take based on the current policy, which could be either exploration or exploitation.
remember(): Stores experiences in memory for future learning.
replay(): Executes experience replay to update the neural network weights.
The model uses a neural network with two hidden layers, each containing 24 neurons, and deploys mean squared error as its loss function for training.

## Average Reward without OR: $8260.56
![OR.png]


## DQN with Operations Research (OR) Implementation Code Description

This extended version incorporates Operations Research techniques to bring a more nuanced approach to ticket pricing. A linear programming objective (lp_objective) is integrated into the decision-making process, optimizing both immediate and long-term objectives.

## Key Functionalities:
act(): Now employs nested_optimization to make balanced action choices, optimizing for both immediate gains and long-term operational objectives.

## Average Reward with OR: $8964.86

Both implementations are powered by TensorFlow for neural network operations and employ Matplotlib for visualizing the rewards across episodes. The OR version additionally utilizes the PuLP library for linear programming tasks.

# Real-world Applications
Finance: Algorithmic trading platforms can employ similar techniques to maximize returns while accounting for risks.
E-commerce: Dynamic pricing strategies can be adapted to e-commerce platforms, balancing inventory levels, competitor pricing, and market demand.
Healthcare: The nested optimization methodology is particularly beneficial in healthcare for developing personalized treatment plans.
Energy Sector: The framework can also be adapted for dynamic pricing and demand-side management in the energy sector, optimizing energy consumption and production in real-time.
