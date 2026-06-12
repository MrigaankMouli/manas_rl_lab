# Algorithms

This directory should contain reinforcement-learning algorithm code.

Expected future files:

- `ppo.py`: PPO update logic, including clipped policy loss, value loss, entropy bonus, gradient clipping, KL tracking, and learning-rate schedule handling.
- `rollout_buffer.py`: storage for observations, actions, rewards, dones, values, log probabilities, advantages, and returns.
- `advantage.py`: generalized advantage estimation and return computation.

If MJLab already provides PPO primitives, keep this directory as a thin adapter layer instead of duplicating the full algorithm.
