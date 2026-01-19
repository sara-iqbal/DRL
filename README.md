# Deep Reinforcement Learning: Navigating the MiniGrid World 🤖

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20RL-orange)
![Environment](https://img.shields.io/badge/Gymnasium-MiniGrid-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

##  Project Overview
Reinforcement Learning (RL) is one of the most fascinating areas of AI, but to truly understand it, you have to build the algorithms from scratch.

In this project, developed in collaboration with **Diana Blokhina**, we explored the full spectrum of RL agents. We started with the mathematical foundations (Dynamic Programming) to solve small grids perfectly. Then, as we scaled up to larger, more complex environments where "perfect" calculation wasn't possible, we transitioned to **Deep Reinforcement Learning**, training Neural Networks to navigate the MiniGrid world.

This wasn't just about using libraries; it was about implementing the logic behind **DQN**, **Double DQN**, and **Policy Gradients** to see how they actually learn.

---

##  The Code & Notebooks
The project is split into two distinct phases. You can explore the code here:

###  Phase 1: The Foundations (Basic Tasks)
**[🔗 View the Basic Tasks Notebook](https://github.com/sara-iqbal/DRL/blob/main/basic_tasks.ipynb)**
* **Focus:** Theoretical understanding and Tabular methods.
* **Algorithms:** Value Iteration, Policy Iteration, Q-Learning, SARSA.
* **Environment:** MiniGrid Empty 6x6.

###  Phase 2: Deep Learning (Advanced Tasks)
**[🔗 View the Advanced Tasks Notebook](https://github.com/sara-iqbal/DRL/blob/main/advanced%20_tasks.ipynb)**
* **Focus:** Function Approximation and Neural Networks.
* **Algorithms:** Deep Q-Networks (DQN), Double DQN, REINFORCE (Policy Gradient).
* **Environment:** MiniGrid 8x8 & Custom Environments.

---

## Tech Stack
* **Python:** Core logic and algorithm implementation.
* **PyTorch:** Building and training the neural networks for the Deep RL agents.
* **Gymnasium (MiniGrid):** The environment wrapper used for the 10 tasks.
* **NumPy:** Handling vector/matrix operations for the tabular Q-tables.
* **Matplotlib:** Visualizing the "Returns vs. Episodes" to track agent convergence.

---

## The 10-Task Challenge
We structured this project as a progression through 10 specific challenges:

### Part 1: Tabular Methods (The "Memory" Approach)
In the beginning, the environments were small enough that we could store every possible state in a table.
* **Tasks 1-3 (Dynamic Programming):** We implemented **Value Iteration** and **Policy Iteration** to calculate the mathematical "Ground Truth" (the perfect path).
* **Tasks 4-6 (Tabular Learning):** We implemented **Q-Learning** (Off-Policy) and **SARSA** (On-Policy). We performed extensive **Hyperparameter Tuning** (Epsilon-Greedy strategies, Learning Rates) to balance exploration vs. exploitation.

<img width="1048" height="527" alt="image" src="https://github.com/user-attachments/assets/c34bbb1a-5d4f-4fef-a32d-e522cd472af4" />


### Part 2: Deep Reinforcement Learning (The "Brain" Approach)
When we increased the grid size to 8x8, the number of states exploded. A simple table wasn't enough, so we used Deep Learning to *approximate* the best moves.
* **Task 7 (DQN):** We built a **Deep Q-Network** using PyTorch. This involved creating a Replay Buffer to store memories and a Target Network to stabilize training.
* **Task 8 (Double DQN):** Standard DQNs often overestimate how good a move is. We implemented **Double DQN** to decouple action selection from evaluation, leading to more stable learning.
  **Task 9 (Policy Gradients):** We moved away from Q-values and implemented **REINFORCE**, an algorithm that learns the policy directly.

### Part 3: The Custom Game
**Task 10 (Gen-RL):** To prove our agents weren't just memorizing one map, we designed a **Custom Environment** with dynamic obstacles and specific objectives to stress-test the robustness of our algorithms.

<img width="467" height="256" alt="image" src="https://github.com/user-attachments/assets/165c7ef2-3177-4676-a0b6-411cd41fafb2" />

---

## Key Results
* **DQN vs. Tabular:** On the 8x8 grid, Tabular Q-learning failed to converge efficiently due to the sparse reward signal. The DQN agent, however, successfully generalized the state space and solved the environment.
* **Stability:** Double DQN provided smoother training curves compared to the volatile learning of the standard DQN.

---

## 👥 Collaborators
* **Sara Iqbal**
* **Diana Blokhina**

