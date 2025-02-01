# SARSA-based Maze Navigation and Pathfinding
This project implements a Reinforcement Learning (RL) algorithm called SARSA (State-Action-Reward-State-Action) to enable an agent to navigate a maze. The objective of the project is for the agent to learn the optimal path from the starting position to the goal position while avoiding obstacles. The agent employs SARSA to explore the maze, accumulate rewards, and update its policy based on its experiences.

*Project Overview*

The agent operates within a 4x4 grid maze, where:
0 represents free space (where the agent can move).
1 represents an obstacle (which the agent must avoid).
2 represents the starting position.
3 represents the goal position.

*Key Components:*

Q-table: A table to store Q-values for each state-action pair. This helps the agent to decide which action to take at each state.
SARSA Algorithm: The algorithm used to update the Q-values based on the rewards received by the agent.
Epsilon-Greedy Policy: Used for balancing exploration and exploitation in action selection.
Visualization: The agent's path is visualized using matplotlib to show the maze and the agent’s movement across episodes.

*How It Works*

Maze Setup: The maze layout is represented as a 4x4 grid. The starting position is marked as 2, and the goal is marked as 3. Obstacles are represented as 1.

*SARSA Training:*

The agent starts at the start position and chooses an action based on the epsilon-greedy policy.

The agent moves to a new state and receives a reward based on the current state (goal, obstacle, or regular step).

The Q-values are updated using the SARSA update rule:

𝑄
(
𝑠
,
𝑎
)=
𝑄
(
𝑠
,
𝑎
)
+
𝛼
(
𝑅
(
𝑠
′
)
+
𝛾
⋅
𝑄
(
𝑠
′
,
𝑎
′
)
−
𝑄
(
𝑠
,
𝑎
)
)

This process is repeated over multiple episodes, and the agent gradually learns the best actions to take to reach the goal.

*Exploration:*

The agent is initially set with a high exploration rate (epsilon = 0.2), allowing it to explore random actions.
Over time, the exploration rate is reduced to allow the agent to exploit the learned actions.
*Visualization:*

After each episode, the agent's path is visualized on the maze grid using matplotlib.
The start position is marked with S, the goal position is marked with G, and the agent’s path is shown as a sequence of red circles.
Example Output
After training, the agent will have learned an optimal policy to navigate the maze. During each episode, the agent explores the maze, learns from its actions, and tries to find the best path to the goal.

*Example output:*

Episode 1 finished.
Episode 2 finished.
Episode 3 finished.
...
Goal reached in 5 steps!
Visualizations of each episode:
The maze grid with the agent's path (red circles) and the start (S) and goal (G) will be plotted after each episode.

*Key Concepts Used*

**SARSA (State-Action-Reward-State-Action):**

This is a reinforcement learning algorithm that updates the Q-value for a given state-action pair after each move. It is on-policy, meaning the agent learns using the actions it actually takes.

**Q-Table:**

A table used to store the agent’s knowledge about the environment. It maps state-action pairs to Q-values, which represent the expected future reward of taking a specific action in a given state.

**Epsilon-Greedy Policy:**

A method to balance between exploring new actions and exploiting the known best actions. With probability epsilon, the agent will choose a random action (explore); otherwise, it will choose the action with the highest Q-value (exploit).

*Author*

This project was developed by *Parvathala Gayathri*. Feel free to explore, modify, and expand upon the code.

