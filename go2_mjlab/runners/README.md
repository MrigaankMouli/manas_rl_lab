# Runners

This directory should contain reusable runner classes that coordinate environments, models, algorithms, logging, checkpoints, and evaluation.

Expected future files:

- `on_policy_runner.py`: main training loop for on-policy algorithms such as PPO. It should reset environments, collect rollouts, sample actions from the actor-critic, call PPO updates, log metrics, save checkpoints, and trigger evaluation hooks.
- `evaluation_runner.py`: deterministic or stochastic policy evaluation loop. It should load checkpoints, run rollout episodes, collect tracking and termination metrics, and optionally support rendering or video capture.

Boundary with other directories:

- `algos/` should contain learning internals such as PPO loss computation, rollout buffers, advantage estimation, optimizer steps, and algorithm-specific state.
- `runners/` should contain the experiment loop that wires together the environment, actor-critic model, algorithm, logging, checkpointing, and evaluation.
- `scripts/` should remain thin command-line wrappers that parse arguments, load configs, construct a runner, and call methods such as `learn()`, or `evaluate()`

The main training entrypoint should eventually look like:

```python
from go2_mjlab.runners.on_policy_runner import OnPolicyRunner

runner = OnPolicyRunner(cfg)
runner.learn()
```

