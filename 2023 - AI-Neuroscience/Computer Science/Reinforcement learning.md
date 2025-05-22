*Reinforcement learning is a fancy trial-and-error*

Reinforcement learning (RL) can be viewed as an approach which falls between _supervised_  and _unsupervised_  learning. It is not strictly supervised as it does not rely only on a set of labelled training data but is not unsupervised learning because we have a reward which we want our agent to maximize

In reinforcement learning the most important thing is the **environment you build and the reward for the agent** [https://youtu.be/A3eWVrM3cvI?t=482](https://youtu.be/A3eWVrM3cvI?t=482)

![[Pasted image 20221005125931.png]]
Agent, environment, action, state and reward flow diagram

## Agent

The agent is the bot itself, the algorithm trying to choose from one decision to another.

“An agent can “interact” with the environment by using a predefined action set . The action set $A = \{A_1, A_2…\}$} describes all possible actions”

For each action the agent takes on the environment, it will win or loose $x$ number of points (reward)

**The goal of the agent is to maximize the cumulative reward**

## Environment

the environment is an entity an agent can interact with, for example the environment could be a pong game. In this scenario, the agent would control the paddle to hit the ball back and forth

✅ “The goal of reinforcement learning algorithms is to teach the agent how to interact “well” with the environment so that the agent is able to obtain a good score under a predefined *evaluation metric*.”

The environment is also divided into _fully observable environment_ and _partially observable environment_.

-   _**Fully Observable Environments** (Markov Decision Process):_ Agent directly observes environment state. $O_t=S_t{^a}=S_t{^e}$
-   _**Partially Observable Environments** (Partially Observable Markov Decision Process):_ Agent indirectly observes environment. $S_t{^a}≠S_t{^e}$

## Action

The input the agent provides to the environment, calculated by applying a policy to the current state

## History

The history $H_t$ is a sequence of observations, actions and rewards up to time $t$. 

## State

The state is the information used to determine what happens next.

The key difference between the _history_ and _state_ is that the state is a function of the history.

$$ S_t = f(H_t) $$

The states can be divided into three main types:

-   _**Environment state** ($S_t{^e}$_) _—_ The environment’s private representation and may not be visible to the agent. It is used to pick the next observation.
    
-   _**Agent State** ($S_t{^a}$_) _—_ The agent’s internal representation and is used by the agent to pick the next action.
    
-   _**Information State** ($S_t$_) _—_ Contains the useful information from the history. Therefore given this state it will be sufficient information to model the future and the history can be thrown away.

## Reward

Based on the action taken from the agent in the environment, a reward $R_t$ is generated. The reward basiclaly tells the agent if the action $A_t$ taken was right or wrong.

## Flow

1. At time $t$, the environment is in state $S_t$
2. The agent observes the current state and select action $A_t$
3. The environment transitions to state $S_{t+1}$ and grants the agent reward $R_{t+1}$
4. This process then starts over for the next time step, $t+1

## Reinforcement Learning algorithms (as of 2022)
![[Pasted image 20221018065739.png]]
Related topics: 
[[Markov Decision Process (MDP)]]