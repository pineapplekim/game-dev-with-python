# Project 3: Blackjack – MC, TD, and Q-Learning

**Language**: Python  
**Library**: PyGame  
_Code not published due to academic integrity policy._

---

## What I Did

- Implemented:
  - Monte Carlo (MC) Policy Evaluation
  - Temporal Difference (TD) Policy Evaluation
  - Q-Learning with ε-greedy strategy (ε=0.4)
- Verified correctness via convergence test on 1M simulations
- Confirmed Q-Learning achieves ~41% win rate in AutoPlay mode

---

## Problems & Solutions

- Implementing One-Step Transitions
  - Problem: When simulating transitions, my previous code didn't properly handle terminal states. Actions continued even after the game ended, leading to undefined rewards and NaN value updates.
  - Solution: In `make_one_transition()`, I checked `game_over()` after each action and returned `None` for next states when terminal. I also used `check_reward()` to capture rewards(+1 for win, -1 for lose, 0 otherwise).

---

## What I Learned

- Exploration vs. Exploitation: Through tuning ε in Q-learning, I saw firsthand how exploration prevents premature convergence but too much randomness slows learning.
- Discounting Future Rewards: I gained intuition for why the discount factor stabilizes value estimates and models long-term strategy.

---

## Demonstration

▶️ [Click here to watch the video on YouTube!](https://youtu.be/TrUcCYFI_p4)
