# StreetFighter-AI



Train a reinforcement learning agent using the PPO algorithm from Stable Baselines 3 to play the Street Fighter game. The project leverages Optuna for hyperparameter optimization to achieve better in-game performance.

## 🚀 Features

Custom environment setup for Street Fighter using Retro.
Frame preprocessing for efficient learning: grayscale conversion, resizing, and channel restructuring.
Hyperparameter tuning using Optuna.
Training using PPO from Stable Baselines 3.
Callbacks for enhanced training visibility and modularity.


## 🛠 Setup

### Dependencies:

All of the necessary packages with the required versions are listed in the notebook. It should also be noted that these packages will ONLY work with python 3.7


## 🎮 Training

### Hyperparameter Optimization
The hyperparameter optimization phase leverages the power of Optuna. Here, we aim to find the best combination of parameters such as 'n_steps', 'gamma', 'learning_rate', 'clip_range', and 'gae_lambda'. This process iteratively tests various combinations to identify the set that produces the maximum reward.



### Model Initialization & Training
Once optimal hyperparameters are identified, the PPO model is initialized using these parameters. Training involves feeding the agent game frames and iteratively updating the model to improve its game-playing strategy. Through this process, the agent learns how to make decisions that maximize its score in Street Fighter.



## 📊 Evaluation

After training, it's essential to evaluate the model's performance. The agent is tested in a series of episodes where it plays the game. We then calculate the mean reward achieved across these episodes to gauge the effectiveness of the trained agent.





## 🔍 Callbacks

To enhance the training process, a custom callback named TrainAndLoggingCallback is utilized. This callback's primary role is to periodically save the model during training. It ensures that progress is captured, allowing for model recovery and resumption of training if required.

## 📈 TensorBoard Visualization

The project has built-in TensorBoard logging capabilities. This tool can be used to visualize various metrics, offering insights into the training progress and potential areas of improvement.


## 🛣 Next Steps

While the current implementation has demonstrated capability in playing Street Fighter, there are several avenues for future enhancements:

1. Objective Refinement: Currently, the training is point-driven, meaning the agent prioritizes accumulating points. This can sometimes make the agent drag a match to three rounds to amass points, even though an efficient win in just two rounds would be ideal. Adapting the model to consider health or other match metrics might offer a more strategic playstyle.
   
2. Level-specific Training: Each opponent in Street Fighter possesses a unique moveset. Training the model specifically for each opponent can fine-tune the agent's strategy, making it adapt better to varied fighting styles.

3. Defensive Rewards: We can further sophisticate our agent by rewarding defensive actions. By incentivizing moves like dodging and blocking, we can craft a more robust and resilient fighter.

4. Efficiency Bonus: To further align with our goal of efficient victories, the agent could receive additional rewards for concluding matches within two rounds, reinforcing the behavior of swift and decisive wins.

Taking these steps can refine the agent's capabilities, transforming it into a formidable Street Fighter player.
