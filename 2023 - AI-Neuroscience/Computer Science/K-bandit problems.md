A k-armed bandit problem (also called multi-armed bandit problem) is a kind of [[Reinforcement learning]] problem where we have to strike a balance netween exploration and explotation of a given set of actions to get the most reward out of many hidden probability distributions.

K-armed bandit problems are reinforcement learning problems with a ***single state***

single-state RL problems are also called *bandits*

watch this video: https://www.youtube.com/watch?v=e3L4VocZnnQ

Obviously in bandit problems distributions can be different, like Gaussian, Bernoulli or others. The idea is to have sufficiently generic algorithm who can maximize the reward (or minimize the regret)

*Regret* is a conccept in RL  problems which is the difference between the optimal reward and the actual reward gained in each round. For example if the maximum reward for an action on the actual state is $1$ but you get $0.7$, then the regret is the difference, which is $0.3$

### Summary of k-bandit problems
1. You have $K$ choices ('arms')
2. Each round (for $T$ rounds) you choose an arm to pull. This gives you a (stochastically/adversarially) generated reward.
3. You want to maximize your total reward
4. Models tradeoff between exploration and exploitation