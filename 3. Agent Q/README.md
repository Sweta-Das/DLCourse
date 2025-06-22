# AgentQ

- Refers to Q-Learning
- It is a fundamental reinforcement learning algorithm.

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
`Q(state, action) = Q(state, action) + α [R + γ * max(Q(next_state)) - Q(state, action)]`

where, </br>
- `α (alpha)` = Learning rate (0 to 1)
- `R` = reward received
- `γ (gamma)` = discount factor (0 to 1)
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
===

## Self-Correction in AgentQ
AgentQ combines the following methodologies to teach agents to self-correct:
1. **Monte-Carlo Tree Search (MCTS)**
    - a decision-making algorithm that combines:
    i. *Tree Search*: Building a search tree of possible future states
    ii. *Random Sampling*: Using random simulations to evaluate decisions
    iii. *Value Estimation*: Calculating expected values of actions

    - Key aspects:
        - Uses 4 steps: **Selection**, **Expansion**, **Simulation**, and **Backpropagation**.
        - Balances exploration vs exploitation
        - Helps agent to make better decisions by looking ahead

2. **Self-Critique Mechanism & Process Supervision**
    This involves 2 main components:
    - **Self-Critique Mechanism**
        - Agent evaluates its own actions
        - Maintains an internal model of success/failure
        - Learns from mistakes through:
            - Action outcome analysis
            - Performance evaluation
            - Strategy adjustment

    - **Process Supervision**
        - Monitors agent's learning process
        - Implements corrective measures when needed
        - Features:
            - Real-time performance tracking
            - Adaptation of learning parameters
            - Error detection and correction

3. **Direct Preference Optimization (DPO)**
    - A training method that directly optimizes the agent's policy based on preference data
    - Key features:
        - Uses pairwise preference comparisons
        - Learns directly from human feedback
        - Optimizes policy without intermediate reward modeling
    - Components:
        - **Preference Dataset**: Collection of paired responses with human preferences
        - **Loss Function**: Specifically designed to optimize policy based on preferences
        - **Direct Policy Updates**: Modifies behavior without intermediate reward models


### References:
https://arxiv.org/abs/2408.07199
https://www.deeplearning.ai/short-courses/reinforcement-learning-from-human-feedback/
https://arxiv.org/abs/2305.18290