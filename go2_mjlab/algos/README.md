# Algorithms

This directory should contain reinforcement-learning algorithm code.

Expected future files:

- `ppo.py`: PPO update logic, including clipped policy loss, value loss, entropy bonus, gradient clipping, KL tracking, and learning-rate schedule handling.
- `rollout_buffer.py`: storage for observations, actions, rewards, dones, values, log probabilities, advantages, and returns.
- `advantage.py`: generalized advantage estimation and return computation.

MJLab already provides PPO primitives, keep this directory as a adaption module layer of the provided Mjlab modules instead of duplicating the full algorithm.
