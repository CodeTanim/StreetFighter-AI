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


## Next Steps
