# Project 2: 2048 AI – Expectimax Search

**Language**: Python  
**Library**: PyGame  
_Code not published due to academic integrity policy._

---

## What I Did

- Implemented an AI player for the game 2048 using **Expectimax Search**
- Built a **depth-3 game tree** where:
  - Max player: the agent
  - Chance player: the computer placing a 2-tile randomly
- Used the **score from the engine** as evaluation value at leaf nodes
- Added optional **extra credit logic** in `compute_decision_ec()` with improved heuristics

---

## Problems & Solutions

- Designing a Depth-3 Game Tree
  - Problem: The core challenge was constructing a depth-3 expectimax tree that alternates between the AI(max player) and the computer(chance player). My initial implementation failed to differentiate between player and chance nodes, causing incorrect value propagation and nonsensical moves.
  - Solution: I modeled node types (`MAX_PLAYER` and `CHANCE_PLAYER`) and handled their value calculations differently:
    - Max nodes choose the move with the highest expected value.
    - Chance nodes compute the average expected value over all possible tile replacements.

- Computing Expected Values for Random Tile Placements
  - Problem: The computer's move involves placing a tile at a random open spot, making the branching factor large. Early versions did not normalize expectations properly, over-estimating the chance player's impact.
  - Solution: I averaged the values of all possible tile placements instead of taking the maximum. This transformed the AI's decision to statistically rational, matching the true expectimax definition.

---

## What I Learned

- Decision-Making under Uncertainty: I learned how expectimax extends minimax to handle randomness and why taking expectations is crucial in stochastic environments.
- Balancing Depth and Performance: I experienced first-hand how increasing search depth improves accuracy but explodes computation, and learned to optimize accordingly.

---

## Demonstration

[▶️ Click here to watch the video on YouTube!](https://youtu.be/cG-FpsGfkfU)
