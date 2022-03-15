# Commitment and Cyclic Strategies in Multi-Objective Games
This repo consists of different agents that were used in our study of commitment and cyclic strategies in multi-objective normal-form games. We model two-player multi-objective Stackelberg games. This code is forked from a previous repository [on communication in multi-objective normal-form games](https://github.com/wilrop/communication_monfg). 

Below, we detail the two new agents that were specifically designed for this work.

## Pessimistic Agent
The pessimistic agent intends to simulate a malicious follower aiming to minimise the leaders utility. Note that this agent can be turned into a positive agent by setting the flag to positive. When this is enabled, the agent will focus only on optimising their own utility.

## Non-Stationary Agent
The leader learns a stochastic policy but commits only to one action in each round. The follower learns a non-stationary policy that is a best-response to the leader's commitment policy *as a whole*. 

## Getting Started

Experiments can be run from the `MONFG.py` file with additional parameters. 
```
usage: MONFG.py [-h] [--game GAME] [--u U [U ...]] [--experiment EXPERIMENT]
                [--alternate ALTERNATE] [--runs RUNS] [--episodes EPISODES]
                [--rollouts ROLLOUTS] [--opt_init]

optional arguments:
  -h, --help            show this help message and exit
  --game GAME           which MONFG game to play
  --u U [U ...]         Which utility functions to use per player
  --experiment EXPERIMENT
                        The experiment to run.
  --alternate ALTERNATE
                        Alternate commitment between players.
  --runs RUNS           number of trials
  --episodes EPISODES   number of episodes
  --rollouts ROLLOUTS   Rollout period for the policies
  --opt_init            optimistic initialization
```

There are 11 MONFGs and 4 utility functions available to pick from. 

## License

This project is licensed under the terms of the MIT license.

