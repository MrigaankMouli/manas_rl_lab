# Configs

This directory should contain user-editable experiment configuration files.

Expected future files:

- `train.yaml`: seed, device, number of environments, rollout length, max iterations, logging, checkpoint frequency, and PPO hyperparameters.
- `env.yaml`: control rate, physics timestep, decimation, episode length, action scaling, observation dimensions, and reset settings.
- `policy.yaml`: actor-critic architecture, actor hidden dimensions, critic hidden dimensions, activation, action standard deviation settings, and observation normalization options.
- `terrain.yaml`: terrain type proportions, difficulty curriculum, roughness ranges, slope settings, and any MJLab terrain generation options.
- `rewards.yaml`: reward weights and reward-specific parameters.
- `randomization.yaml`: friction, mass, actuator, sensor noise, and external disturbance randomization ranges.

Keep configs declarative. Implementation logic should live in `go2_mjlab/`, not in YAML files.
