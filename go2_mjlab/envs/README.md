# Environments

This directory should contain the MJLab environment implementation and environment-side building blocks.

Expected future files:

- `go2_rough_env.py`: main MJLab environment class. It should load the Go2 model, reset simulation state, apply actions, step physics, assemble observations, compute rewards, compute terminations, and return the standard RL step tuple.
- `observations.py`: deployable observation construction. Start with proprioceptive observations such as base angular velocity, projected gravity, commands, joint position errors, joint velocities, and previous actions.
- `rewards.py`: reward term implementations and reward aggregation. Port the important IsaacLab reward ideas here: velocity tracking, orientation stability, torque cost, action-rate cost, foot slip, stand-still penalties, and joint regularization.
- `terminations.py`: timeout, base contact, bad orientation, low base clearance, and low-progress termination logic.
- `randomization.py`: domain randomization for friction, base mass, actuator stiffness, actuator damping, sensor noise, and disturbances.
- `terrain.py`: terrain generation or terrain loading utilities for rough ground, slopes, boxes, stairs, and curriculum difficulty.
- `commands.py`: velocity command sampling and command curriculum logic.

Environment code should not know PPO parameters. It should only provide clean observations, rewards, terminations etc.
