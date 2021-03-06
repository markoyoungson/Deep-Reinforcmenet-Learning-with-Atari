# Deep-Reinforcement-Learning-with-Atari

Hey everyone!
Here I will be showing all my code for my project on creating an Agent to play atari games.










If you want a more in depth break down of the code and reasoning behind it check out my [article](https://mark-youngson5.medium.com/so-you-want-to-play-atari-games-e9252762a142) I wrote on it!

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [What is Deep RL?](#What-is-Deep-RL?)
* [My Code Breakdown](#My-Code-Breakdown)

## General info
This project was inspired by the research paper [Human Level Control Through Deep Reinforcement Learning](https://drive.google.com/viewerng/viewer?url=https://web.stanford.edu/class/psych209/Readings/MnihEtAlHassibis15NatureControlDeepRL.pdf) written by Google DeepMind in 2015
	
	
	
## Technologies
Project is created with:
* Python version: 3.6.7
* Pytorch version: 1.0.0
* Numpy: 1.16.4



## What is Deep RL?
Before we get into any of the details, let me first explain what is going on.

The goal of an RL problem is to create a agent that maximizes some reward in an environment. In this case we are trying to get the agent to maximize the amount of points it can get in Pong(Atari Games). The environment is the game that the agent is playing, and to receive rewards it has to take an action. There are many different algorithmns that can get the agent to maximize its long term reward. A very common example would be Q learning. In this example after every action the agent takes in its environment, it receives a reward and a new state, and it stores all this information in what is called a Q table. After thousands of iterations the agent will have mapped out all the possible actions, and in turn all of the rewards. The agent then can take the action that gives the agent the greates reward. 

The problem with that approach is that you have to store all of the agents experiences in a Q-table. So what Deep Reinforcment learning does is that instead of mapping out all of the experineces, you use a convolutional neraual network to take in the image pixels and output the value that each action would give the agent. So in pong the different actions would be moving the paddle up, down and staying in the same place. The agent than takes the action with the highest value in every state.

Like I mentioned before, I have a much more in depth breakdown of this in my article that is linked above.


## My Code Breakdown

My Code is broken down into 5 main sections:

* The Utils File: Here we deal with the pre-processing the image data

* The Replay Memory: In this file we store the agents past experiences

* The Neural Net: This file has the Convolutional Neural Network that takes in the image data and outputs the value for each action in a state

* The Agent: In this file you initailize the agents parameters, and define the learn function, so that the agent is able to learn from its experiences

* The Main File: Finanlly, we bring everything together
