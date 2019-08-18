# chrome-dino-ai

## Chrome-Dino run game using Deep Q Network and Reinforcement Learning

#### Elucidation of Problem
	
Dino Run is a runner game in Chrome browser which appears when the browser is offline. We plan to create a DQN to play this game automatically by learning action patterns from image input using Reinforcement Learning Algorithm.

The aim of the game is to make dino avoid the danger of cactus and animal birds.
The reward of the game is to keep dino alive by dodging mentioned dangers. Each successful dodge will reward you with points.
Based on the observed patterns and self-learning, reinforcement agent will learn to act by choosing one of the following actions:
- Jump
- No jump
<img src = "https://www.androidpolice.com/wp-content/uploads/2018/11/chrome-dino-hero.png" width="400">

#### Suggested Method
We will be using DQN for Q function approximation. During the gameplay simulations, we will stack 4 immediate frames of the gameplay together and we will let Target Network (TN) decide the action on that stack of frames. We aim to train the Deep Q Network (DQN) by back propagating the difference between the approximated and computed Q values for a given state and an action. 
We will be trying out few tricks suggested by Google DeepMind’s research paper on Reinforcement Learning like having an experience replay buffer, gradually decreasing random exploration and keeping TN and DQN separate (after T episodes,  another hyperparameter, TN will borrow the weights from DQN) to keep the approximation of Q values stable at each step. We will follow an empirical process to settle for the best values of hyperparameters which maximizes the game score.

## Getting Started


### Prerequisites

* Python 3.0
* Jupyter

### Installing

    git clone https://github.com/poojathakoor/chrome-dino-ai.git
    cd chrome-dino-ai/chrome-dino-ai

## Demo

![](demo.gif)

## Miscellaneous

* Report[report.pdf]
* Presentation[presentation.pdf]

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details

## Authors

* **Pooja Thakoor** - [Pooja Thakoor](https://github.com/poojathakoor)
* **Yogesh Jadhav** - [Yogesh Jadhav](https://github.com/yogeshjadhav7)
* **Sameer Shinde** - [Sameer Shinde](https://github.com/sameershinde14)
