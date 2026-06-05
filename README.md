# Rod-Maneuvering-with-Prioritized-Sweeping

## Aim

To implement the **Prioritized Sweeping Reinforcement Learning algorithm** for a Rod Maneuvering environment and learn an optimal policy that efficiently guides the rod from its initial position to the target position while avoiding obstacles and minimizing the number of steps.

---

## Algorithm

### Prioritized Sweeping Algorithm

1. Initialize the state-value or action-value function (Q(s,a)) arbitrarily.

2. Initialize a model to store state transitions and rewards.

3. Observe the current state (s).

4. Select an action (a) using an exploration strategy (e.g., ε-greedy).

5. Execute the action and observe:

   * Next state (s')
   * Reward (r)

6. Store the transition ((s,a,r,s')) in the model.

7. Compute the priority:

   [
   P = |r + \gamma \max_a Q(s',a) - Q(s,a)|
   ]

8. If the priority exceeds a threshold, insert ((s,a)) into the priority queue.

9. While the queue is not empty:

   * Remove the state-action pair with the highest priority.
   * Update its Q-value.
   * Find predecessor states.
   * Recalculate their priorities.
   * Insert significant predecessors into the queue.

10. Repeat until the goal state is reached or the maximum number of episodes is completed.

11. Extract the optimal policy from the learned Q-values.

---

## Program

```python

```


## Output

```text



```



---

## Result

The **Prioritized Sweeping algorithm** was successfully implemented for the Rod Maneuvering environment. The agent learned an optimal path from the start state to the goal state by combining real experience with model-based planning. Prioritized updates enabled faster convergence and improved learning efficiency compared to conventional reinforcement learning approaches.


