# Safe-DRL-Autonomous-Vehicles

This repository explores **Safe Deep Reinforcement Learning (DRL) for Autonomous Vehicles**, focusing on the impact of computation delay in reinforcement learning-based driving environments.

## Overview
This project implements the **`highway-v1`** environment to improve continuous action spaces (from highway-env) and introduces computation delay effects. The goal is to evaluate how delays impact DRL models in autonomous driving, with experiments on algorithms like **DQN, PPO, and DDPG**.

## Features
- **Custom `highway-v1` environment** improves continuous control.
- **Computation delay simulation** with exponential and fixed delays.
- **DRL algorithms** (DQN, PPO for discrete; DDPG for continuous).
- **Performance analysis** under different delay conditions.

## Installation
## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Chihehehe/Safe-DRL-Autonomous-Vehicles.git
   ```
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Run the `.ipynb` file step by step to train and evaluate DRL models under computation delay.

## Results
The results analyze **reward trends, crash rates, and performance drops** under different computation delays. See the **report** for detailed insights.
