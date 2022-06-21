## Reinforcement Learning

Interact with the environment and improve performance trial-and-error based.

# Portfolio Management Problem

Definition: Invest into a set of assets and reallocate in a fixed period (eg. one year)

Assumptions
- Market is continuous: 종가 = 시가
- Reallocation is done at the end of the day
- Transaction cost is considered (0.25%)
- Portfolio consists of m+1 assets: m risky, 1 risk-free (cash)

Notations
- $v^{close}_{i,t}$ : closing price of ith asset after time t. 
- $S$ : set of states
- $A$ : set of actions
- $P$ : transition probability distribution
- $r : S \rightarrow R$ : reward function
- $\rho_0$ : distribution of initial state
- $\gamma \in (0,1)$ : discount factor

Wealth of a portfolio at time T is the product $$\large\prod_{t=1}^{T}{\gamma^tr(s_t,a_t)}$$

# Deep Reinforcement Learning

Why neural network?

1. Machine-defined inputs and outputs

Market information can be encoded as inputs and allocation vector as outputs. This allows for end-to-end training without hand crafted features.

2. Implicit predictions on stock performances

Reinforcement learning avoids explicit predictions of stock performances, reducing complexity of the problem.

3. Free from curse of dimensionality

DRL approximates various strategies and value functions, empowering large-scale portfolio management

## Deep Deterministic Policy Gradient (DDPG)

Combination of Q-learning and policy gradient.

### Q-learning

- Def: Reinforcement learning based on Q-Value function
  - Q-Value function: expected accumulated reward when executing action a in state s and follow policy pi in the future.
  - $$Q^\pi(s_t,a_t)=$$
