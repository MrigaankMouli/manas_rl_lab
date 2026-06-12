# Project MANAS Unitree Go2 RL Repository

This repository is intended to act a base mjlab implementation of the Go2 terrain locomotion project by Project MANAS.

The initial base implementation should follow a simple architecture:

- one Go2 rough-terrain environment
- one PPO-style training loop
- one actor-critic policy
- actor and critic as configurable MLPs
- clean export and evaluation paths

The directories below separate simulation, robot metadata, model code, training code, export utilities, configs, scripts and tests.

The project should follow the following directory structure:

1. `configs/` defines the experiment.
2. `go2_mjlab/envs/` builds observations, rewards, terminations, commands, randomization, and terrain.
3. `go2_mjlab/models/` defines the MLP actor-critic.
4. `go2_mjlab/algos/` updates the policy with PPO.
5. `go2_mjlab/runners/` connects env, model, algorithm, logging, and checkpoints.
6. `scripts/` provides thin command-line entrypoints.
7. `go2_mjlab/export/` produces deployment artifacts --> This should be the Last TODO undertaken, after the base policy has been trained and evaluated on mujoco(also consider sim2sim evaluation before sim2real evaluation).
