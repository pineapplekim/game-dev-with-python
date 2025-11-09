# Project 4: Gomoku AI with Monte Carlo Tree Search

**Language**: Python    
_Code not published due to academic integrity policy._

---

## What I Did
- Implemented an AI for Gomoku using **Monte Carlo Tree Search (MCTS)**
- MCTS returns not only the best move but also a **table of estimated win rates** per action
- AI was tested with:
  - Predefined game states
  - Self-play against a random AI agent

---

## Problems & Solutions

- Implementing the Four Core Steps of MCTS
  - Problem: Understanding how Selection, Expansion, Simulation (Rollout), and Backpropagation connect was difficult at first. My loop would either never terminate or update wins incorrectly.
  - Solution: I modularized each step:
    - `select()` uses UCB with `c = 1` to choose the most promising child.
    - `expand()` creates a new child from an untried move.
    - `rollout()` uses random moves until the game ends.
    - `backpropagate()` updates win counts for the parent's player, as required by the spec.

---

## What I Learned

- Monte Carlo Tree Search Mechanics: I gained a deep understanding of how simulation statistics guide decision-making under uncertainty.
- Determinism in AI Testing: Realized how fixed ordering and random-seed control are vital for reproducible grading.

---

## Demonstration
[▶️ Click here to watch the video on YouTube](https://youtube.com/shorts/3TuKmqPcdMQ?feature=share)
