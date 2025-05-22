Bellman equation is part of [[Dynamic programming]] paradigm and its purpose is to yield the best decision at any given point in time to maximize the future reward. It is used to solve  [[Markov Decision Process (MDP)]] and finding optimal policy and value function.

Bellman equation uses the same concepts as [[Reinforcement learning]] which are STATE, ACTION, REWARD, VALUE and $\gamma$ which is discount factor

## Formal Equation (for deterministic environments)
$V(s)={max}_{a}(R(s,a)+\gamma V(s'))$

What Bellman Equation is for:
1. What is the VALUE of the current state?
2. helps us evaluate the expected reward relative to the advantage or disadvantage of each state