AI Snake Game Project

This is an AI-powered Snake Game that uses Reinforcement Learning and a Neural Network to play. In this game, an agent is trained using Q-Learning, a popular Reinforcement Learning technique, to maximize its score. The project has two main files:

agent.py: This file contains the implementation of the Agent class. The Agent class defines the behavior and state of the snake, and how it should interact with the game board. The get_state() method gets the current state of the game, get_action() method takes the current state and returns an action, and the remember() method stores the transition of the game state. The train_short_memory() method updates the weights of the model for the current game state, and the train_long_memory() method trains the model using experiences stored in the memory.
game.py: This file defines the SnakeGameAI class, which runs the game environment. It contains the implementation of the game loop, which continuously updates the state of the game, and the play_step() method, which performs one step of the game by taking an action and returning the new state of the game.
How to run

To run the game, simply run the agent.py file. The game will start running and will automatically train the agent to play the game. The game will be displayed using the Pygame library.

Dependencies

The following dependencies are required to run the project:

Pygame
NumPy
PyTorch



Kevin Rollins Rollins
Please rewrite the readme further describing each file
Sure, here's a revised version of the readme:

AI Snake Game Project

This is a simple Snake game developed using Pygame library in Python. The game features an AI agent that is trained to play the game using Q-learning algorithm.

Files
Agent.py

This file contains the Agent class which represents the AI agent in the game. The agent is initialized with a number of hyperparameters such as the maximum memory to store in the memory buffer, batch size, learning rate, etc.

The agent contains several methods including:

get_state: This method takes the current game state as input and returns an array representing the state that can be used as input to the agent's neural network.
remember: This method takes the current state, action, reward, next state, and game over flag as input and stores them in the memory buffer.
train_long_memory: This method samples a batch of experiences from the memory buffer and trains the agent's neural network using the Q-learning algorithm.
train_short_memory: This method trains the agent's neural network on a single experience.
get_action: This method takes the current state as input and returns the agent's action (up, down, or left) based on its current policy.
Game.py

This file contains the SnakeGameAI class which represents the Snake game. The game features a snake that moves around the game board and tries to eat food. The game ends when the snake collides with a wall or its own body.

The class contains several methods including:

play_step: This method takes the agent's action as input and performs a single step in the game, updating the game state and returning the reward, game over flag, and current score.
get_state: This method returns the current game state as an array that can be used as input to the agent's neural network.
Model.py

This file contains the Linear_QNet class which represents the agent's neural network. The neural network consists of a single linear layer that takes the game state as input and outputs the Q-values for each possible action.

Helper.py

This file contains the plot function which is used to plot the scores and mean scores during training.

How to Run
To run the game, simply execute the train() function in the Agent.py file. This will start the training process and display the game window.

Dependencies
This project requires the following Python libraries to be installed:

Pygame
Torch
NumPy
