# Robots

This directory should contain Go2-specific robot metadata and asset references.

Expected future files:

- `go2.py`: joint names, joint order, default joint positions, action order, torque limits, foot body names, base body name, control gains, observation indexing helpers, and robot-specific constants.
- `assets/`: MJCF, mesh, and texture files used by MJLab.

Keep robot constants centralized here so environment, reward, and export code do not duplicate joint ordering or body naming assumptions. The required files can be ported from the existing unitree_rl_mjlab repository.
