# Tests

This directory should contain focused tests for the MJLab port.

Expected future files:

- `test_actor_critic.py`: verify actor output shape, critic output shape, log-probability shape, deterministic inference, and configurable hidden dimensions.
- `test_observations.py`: verify observation dimensions, ordering, finite values, and reset behavior.
- `test_rewards.py`: verify reward terms have expected signs and shapes.
- `test_terminations.py`: verify timeout, bad orientation, base contact, and low-progress conditions.
- `test_env_step.py`: smoke-test reset and one environment step.
- `test_export.py`: verify exported policy accepts the declared observation shape and returns the declared action shape.

Prefer small shape and behavior tests first. Full training tests can be added later as slower integration checks.
