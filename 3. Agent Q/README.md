# AgentQ

- Refers to Q-Learning
- It is a fundamental reinforcement learning algorithm.
</br>

### Definition
Q-learning is a model-free reinforcement learning algorithm that learns to make decisions by discovering which actions are most valuable in which states.

### Key Components
1. **Q-Table**

    - A lookup table that stores the expected reward (Q-value) for each state-action pair.
    - Helps the agent to determine the best action in any given state.

2. **Learning Process**

    - The agent interacts with the environment.
    - For each action, it receives a reward.
    - Updates Q-values using the Bellman equation.

### Q-Learning Formula
`Q(state, action) = Q(state, action) + $\alpha$[R + $\gamma$ * max(Q(next_state)) - Q(state, action)]`

where,
    - `$\alpha$ (alpha)` = Learning rate (0 to 1)
    - `R` = reward received
    - `$\gamma$ (gamma)` = discount factor (0 to 1)
    - `max(Q(next_state))` = maximum predicted rewards for the next state

### Advantages
- Works without a model of the environment
- Can handle stochastic environments (environment where same action can result into varying outputs)
- Learns optimal policy throughout trial and error
- Balances exploration and exploitation

### Limitations
- Can be slow to converge; meaning it can be slow to learn the optimal strategy to accurately estimate q-values for all (or most) state-action pairs
- Struggles with large state spaces
- Requires discrete state-action spaces
- Memory intensive for complex environments

