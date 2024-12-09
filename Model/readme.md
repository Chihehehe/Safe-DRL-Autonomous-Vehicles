A2C
![image](https://github.com/user-attachments/assets/2d92dbe7-cff1-48d7-9cd2-9ec4413bb428)
![image](https://github.com/user-attachments/assets/a9cd4a1a-c7fb-4561-911d-3abdd6b8c5f2)


DDPG
![image](https://github.com/user-attachments/assets/898012cc-c7a3-4bd2-bad3-af5cc05dd7f9)

![image](https://github.com/user-attachments/assets/9fa9f82d-4bac-40fa-b644-80d9f7cb3554)


SAC
![image](https://github.com/user-attachments/assets/f81a968b-8c56-46f4-8b35-d13bfabdf071)

![image](https://github.com/user-attachments/assets/a0ebde22-c5ad-4ee8-977a-1295216af9e3)


TD3
![image](https://github.com/user-attachments/assets/fe6abc08-159e-4c29-b17d-a4b4436c1fcd)

![image](https://github.com/user-attachments/assets/9ea047fd-1367-4ccd-8441-c449ea1161fe)


PPO
![image](https://github.com/user-attachments/assets/c6ad449d-7c97-452e-aae0-98da6bea94d3)

![image](https://github.com/user-attachments/assets/819454d2-3b91-46a4-8771-70916dad92ca)



# Highway Environment - Reinforcement Learning Agent Comparison

This repository contains the implementation of various reinforcement learning algorithms for training agents in the `highway-v0` environment. The goal is to train high-performing agents capable of navigating a highway safely, efficiently, and effectively.

## Algorithms Compared

The following RL algorithms were implemented and evaluated:

1. **A2C (Advantage Actor-Critic)**  
2. **DDPG (Deep Deterministic Policy Gradient)**  
3. **SAC (Soft Actor-Critic)**  
4. **TD3 (Twin Delayed Deep Deterministic Policy Gradient)**  
5. **PPO (Proximal Policy Optimization)**  

---

## Environment Details

The training environment is based on `highway-v0` from the `highway-env` library. Agents are required to learn behaviors such as staying on the road, maintaining safe distances, and avoiding collisions while optimizing for rewards.

### Configuration:
- **Action Space**: Continuous
- **Simulation Frequency**: 15 steps per second

---

## Reward Function

The reward function encourages desirable behaviors such as:
- Staying on the road.
- Maintaining a target speed.
- Avoiding collisions.
- Penalizing undesirable behaviors like going off-road or jerky movements.


## Results and Comparisons

### Metrics Evaluated:
1. **Episode Length (`rollout/ep_len_mean`)**: Measures how long the agent survives in an episode.
2. **Reward (`rollout/ep_rew_mean`)**: Average reward earned by the agent per episode.

### Performance Summary:

| Algorithm | Avg. Episode Length | Avg. Reward | Observations                          |
|-----------|----------------------|-------------|---------------------------------------|
| **A2C**   | ~40                 | ~19         | Stable but rewards plateau early.     |
| **DDPG**  | ~39.6               | ~25         | High rewards but more fluctuations.   |
| **SAC**   | ~39.8               | ~24         | Good performance with some variance.  |
| **TD3**   | **~40**             | **~28**     | Best performance overall.             |
| **PPO**   | ~39.9               | ~22         | Stable but slightly lower rewards.    |

### Key Insights:
- **TD3** achieved the highest average reward (~28) and maintained near-max episode lengths (~40).
- **A2C** and **PPO** were stable but offered lower rewards compared to DDPG and TD3.
- **DDPG** displayed strong rewards but had higher fluctuations, requiring careful tuning.
