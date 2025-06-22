# Agent Q (Browser MCTS)

## Browser World Model
Models the browser environment handling;
- State representation (DOM, URL, objective)
- Action execution (clicking, typing, navigation)
- State transitions

## Browser MCTS
Orchestrates the entire process:
- Initializes the world model and search configuration
- Runs the MCTS algorithm
- Generates Q-reward values for DPO