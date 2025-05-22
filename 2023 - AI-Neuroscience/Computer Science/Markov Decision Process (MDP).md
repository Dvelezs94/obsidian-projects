The Markov Decision Process is a control process framework for modeling decision-making situations where outcomes are partly random and partly under the control of a decision maker (agent).

The Goal of MDP is to **find a good "policy" for the decision maker**, a function $\pi$ (often a lookup table) that specifies the action $\pi(s)$ that the decision maker will choose when in state $s$. 

MDPs are an extension of [Markov Chains](https://en.wikipedia.org/wiki/Markov_chain) with aditions of actions and rewards.

MDP is just a mathematical framework. Many algorithms and equations are based on this same framework, that is why it is so useful to understand it.

MDPs are part of the foundational theory in [[Reinforcement learning]] 

## Elements
MDP is a 4-tuple $(S, A, P_a, R_a)$, where
- $S$ Set of states called *state space*
- $A$ Set of actions called *action space* (Alternatively $A_s$ is a set of actions available from that state $s$)
- $P_a(s, s')$ = $Pr(s_{t+1} = s'|s_t=s,a_t=a)$ is the probability that action $a$ in the state $s$ at time $t$ will lead to state $s'$ at time $t+1$. Again,  it is just the probability of being on that next state given the action.
- $R_a(s, s')$ immediate reward (or expected immediate reward) received after transitioning from state $s$ to the state $s'$, due to action $a$

![[Pasted image 20221031165848.png]]
Example of a simple MDP with three states (green circles) and two actions (orange circles), with two rewards (orange arrows).

## Types of MDPs
### Finite
In a finite MDP, the sets  $S,A \text{ and } R$ are finite. Example a maze
### Infinite
In an infinite MDP, one or more sets mentioned above, are infinite. Example when you drive a car, the set of actions can be infinite (e.g. velocity: 70km/h, 70.1 km/h, 70.11 km/h...)
### Episodic
Episodic MDPs stop when a certain state is reached. Example in chess when a you do a check-mate
### Continuing
Continuing MDPs dont have a termination condition, it just keeps going. Example is a trading bot who constantly learns new patterns to buy and sell stocks


## Simulator models
TBD


## Reward and Return

## Discount Factor
Many MDP equations include a discount factor dennoted by the greek letter gamma $\gamma$. This discount factor is used as a knob to take **future** state-action rewards into consideration

where: $$G_0 = R_1 + \gamma R_2, + \gamma^2 R_3, + \gamma^3 R_4 + \text{...}+\gamma^{T-t-1}R_t$ where $\gamma \in [0,1]$$ 

We want to maximize the long-term sum of discounted sum of rewards.

## Policy
The policy is the set of actions to take in a particular state

Probability of taking action $a$ in state $s$ 
$$\pi(a|s)$$

Action $a$ staken in state $s$
$$\pi(s)$$

### Types of policies

**Stochastic**
Stochastic policies gives you the probability distribution of actions
$$\pi(s) = [p(a_1), p(a_2),...,p(a_n)]$$
$$\pi(s) = [0.3, 0.2, 0.5]$$
**Deterministic**
Deterministic policies give you a fixed action given a state
$$\pi(s) \rightarrow a$$
$$\pi(s) = a_1$$
The policy is key, as we mentioned above we want to maximize the sum of discounted rewards, so in order to do that we must **find the optimal policy** $\pi*$
