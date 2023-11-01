# Ticket Pricing Strategy with DQN and Operations Research
## Overview
This repository contains Python code that employs both Deep Q-Network (DQN) and Operations Research (OR) methods to optimize ticket pricing strategies. The code provides an environment for simulating ticket sales, taking into account various parameters like days left for the event, tickets left, and current price.

## Results
After running both approaches through multiple episodes, the average rewards achieved are as follows:

## Average reward without OR: 8260.56
## Average reward with OR: 8964.86
The results indicate that incorporating Operations Research techniques into the DQN framework yields a more effective pricing strategy.

Requirements
Python 3.x
NumPy
TensorFlow
PuLP
Setup
To run the code, first install the required packages:

bash
Copy code
pip install numpy tensorflow pulp
How to Run
Simply execute the Python script for running the simulation:

bash
Copy code
python ticket_pricing_dqn_or.py
Feel free to modify parameters and run additional experiments to further explore the effectiveness of the DQN and OR methods in optimizing ticket pricing strategies.
