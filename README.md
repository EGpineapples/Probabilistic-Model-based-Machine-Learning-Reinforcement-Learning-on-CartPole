# Probabilistic Model-based Machine Learning: Reinforcement Learning on CartPole

![CartPole Reinforcement Learning](https://developer.ridgerun.com/wiki/images/f/f5/Jetson_reinforcement_cartpole.gif)

## Abstract

This project enhances Reinforcement Learning (RL) agents' performance by incorporating text information in game environments. We developed a Bayesian neural network with hierarchical weights, using web-scraped game walkthroughs and latent Dirichlet allocation (LDA) for topic extraction. Experiments were conducted using OpenAI Gym's CartPole-v1 environment.

## Background

Reinforcement Learning shows promise for training intelligent agents in video games. We consider a simple RL Probabilistic Graphical Model (PGM) and validate that RL is possible using Stochastic Variational Inference (SVI) in this framework.

## Data

We utilized three datasets:
1. CartPole-v1 environment from OpenAI's gym library
2. Self-play dataset generated through RL
3. Text dataset scraped from websites related to the CartPole framework

## Modelling Approach

### Generative Process and PGM

Our approach involves:
1. Drawing global parameters
2. Specifying level-specific coefficients
3. Applying transformations to generate observations
4. Incorporating word embeddings
5. Applying a hierarchical model with non-linear activation

### Topic Modelling with LDA

We used Latent Dirichlet Allocation (LDA) for analyzing web-scraped text data, uncovering latent topics and their associations with words.

## Deep Q-Network (DQN)

We implemented a DQN using PyTorch and Pyro, combining a PGM with a neural network. The architecture includes:
- Feed-Forward Neural Network (FFNN) with three fully connected layers
- Hierarchical global and local weights
- Word embedding layer

## Results

Our experiments compared DQN and ComparisonDQN algorithms, showing comparable performance in the CartPole-v1 environment. Both algorithms demonstrated significant improvements over random self-play.

## Conclusion

The integration of textual knowledge, hierarchical weights, and Bayesian modeling proved effective in improving decision-making and enhancing the overall performance of the DQN agent in the CartPole task.
