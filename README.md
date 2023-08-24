# StreetFighter-AI

This project aims to build a reinforcement learning agent capable of playing the Street Fighter game. Using the PPO algorithm from Stable Baselines 3, the agent is trained to maximize its score in the game environment. The hyperparameters for the model are optimized using the Optuna framework.

Table of Contents

Project Structure
Setup
Training
Evaluation
Project Structure

Environment Setup:
The environment (StreetFighter) is a custom-defined class that initializes the Street Fighter game, preprocesses frames for the AI, and handles steps (actions) taken by the AI.
Hyperparameter Optimization:
Optuna is employed to optimize hyperparameters like n_steps, gamma, learning_rate, clip_range, and gae_lambda.
Training the Model:
The PPO algorithm from Stable Baselines 3 is used to train the agent. Training configurations are adjusted based on hyperparameter optimization results.
Evaluation:
After training, the model's performance is evaluated based on the mean reward achieved in the game environment.
Setup

Dependencies
