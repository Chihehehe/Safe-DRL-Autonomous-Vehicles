In my project, I worked with the merge-v0 and intersection-v0 environments using the TD3 algorithm to train autonomous driving agents. In merge-v0, the initial no-crash rate during training was around 29%, which improved to 37% after fine-tuning. During testing, the model achieved a much higher 94% success rate, showing strong generalization. For intersection-v0, the no-crash rate during training reached 60%, but maintaining higher safety levels in this environment proved more challenging.
To improve the models, I explored multiple strategies. On the model side, I adjusted hyperparameters like action noise, buffer size, and learning rate, and I experimented with neural networks by changing the number of layers, neurons, and activation functions. On the environment side, I modified the reward structure by increasing penalties for collisions and boosting rewards for successful behaviors, such as safely navigating the intersection or merging. Additionally, I tested different configurations of traffic density and vehicle behavior to make the scenarios more manageable.
Despite these efforts, the improvements in performance were incremental. For merge-v0, the model generalized well during testing but struggled during training, with limited improvement in the no-crash rate. For intersection-v0, while the agent performed moderately well, crashes remained an issue. These results suggest the environments are inherently complex, and achieving perfect performance requires further research into more advanced techniques, such as reward shaping, transfer learning, or alternative RL algorithms like SAC or PPO.

Merge:
![image](https://github.com/user-attachments/assets/401e12ef-6fcc-4d92-b23c-1491d8834f54)
![image](https://github.com/user-attachments/assets/2f2cca1c-f364-4aed-a974-0e7586aa0bb2)

Intersection:
![image](https://github.com/user-attachments/assets/be2c43ce-5d39-4ce3-8671-1bdaa0e6f48d)
![image](https://github.com/user-attachments/assets/091bf114-0060-4d22-99ef-057d004600f3)

