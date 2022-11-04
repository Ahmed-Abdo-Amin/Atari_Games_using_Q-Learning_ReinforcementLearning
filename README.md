# Atari Games using Q-Learning (Reinforcement Learning)


## Problem Statement: 
There are 4 locations (labeled by different letters), and our job is to pick up the passenger at one location and drop him off at another. We receive +20 points for a successful drop-off and lose 1 point for every time-step it takes. There is also a 10 points penalty for illegal pick-up and drop-off actions.

## Instructions:

    1- Turn this code into a module of functions that can use multiple environments.
    2- Tune alpha, gamma, and/or epsilon using a decay over episodes
    3- Implement a grid search to discover the best hyperparameters

## Solutions:
      
    First, some python Development must be installed such as '!pip install cmake 'gym' scipy'.
    Second, some libraries must be imported such as 'import gym', 'from numpy import array', 
    'from IPython.display import clear_output', and others.

    It was created brute-force function and Q-learning function
    to get the average timesteps for going the target in some environments.
    
Steps to achieve the target in this environment by using Q-learning (Reinforcement Learning):
    
    1- Some hyperparameters (alpha, gamma, and epsilon) were created by special range to get the smallest average timesteps per episode.
       by using numpy.np.linspace(start,end, iteration) such as 'np.linspace(0.1,0.2,2)'
    2- All values of hyperparameters were put in lists. 
    3- All probabilities of lists (alpha, gamma, and epsilon) were created.
            0.1  0.6 0.1
            0.1  0.6 0.2
            0.1  0.3 0.1
            0.1  0.3 0.2
            0.2  0.6 0.1
            0.2  0.6 0.2
            0.2  0.3 0.1
            0.2  0.3 0.2 
    4- 'Taxi-v3' environment was created such as 'env = gym.make("Taxi-v3")' to give Q-learning funcation.
    5- It was used loop (for loop) for all probabilities of hyperparameters in training and Evaluating to get the best probability for hyperparameters.
       	Alpha	Gamma	epsilon	Average timesteps per episode
      0	0.1  	0.6	     0.1	12.64
      1	0.1	    0.6	     0.2	12.91
      2	0.1	    0.3	     0.1	12.91
      3 0.1	    0.3	     0.2	13.30
      4	0.2	    0.6	     0.1	12.26
      5	0.2	    0.6	     0.2	12.85
      6	0.2	    0.3	     0.1	12.95
      7	0.2	    0.3	     0.2	13.36
       
    6- To get the smallest average timesteps per episode.
       
       Alpha	0.10
       Gamma	0.30
       epsilon	0.10
       Average timesteps per episode	12.26
