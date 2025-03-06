# Safe-DRL-Autonomous-Vehicles

This repository explores **Safe Deep Reinforcement Learning (DRL) for Autonomous Vehicles**, focusing on the impact of computation delay in reinforcement learning-based driving environments.

## Overview
This project extends the **`highway-env`** environment to support continuous action spaces (`highway-v1`) and introduces computation delay effects. The goal is to evaluate how delays impact DRL models in autonomous driving, with experiments on algorithms like **DQN, PPO, TD3, and DDPG**.

## Features
- **Custom `highway-v1` environment** supporting continuous control.
- **Computation delay simulation** with exponential and fixed delays.
- **Comparison of DRL algorithms** (DQN, PPO for discrete; DDPG, TD3 for continuous).
- **Performance analysis** under different delay conditions.

## Installation
### 1. Clone the repository
```bash
git clone https://github.com/Chihehehe/Safe-DRL-Autonomous-Vehicles.git
cd Safe-DRL-Autonomous-Vehicles
```
### 2. Install dependencies
```bash
pip install -r requirements.txt
```

## Usage
### Train a DRL agent
Modify `config.py` to select an algorithm, then run:
```bash
python train.py --env highway-v1 --algo DDPG
```
### Test a trained agent
```bash
python test.py --env highway-v1 --model path_to_model
```

## Results
The results analyze **reward trends, crash rates, and performance drops** under different computation delays. See the **report** for detailed insights.
