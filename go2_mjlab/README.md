# Python Package

This directory should contain the importable MJLab Go2 locomotion package.

The package should expose environment creation, actor-critic construction, training runners, export utilities, and shared helpers.

Expected future package modules:

- `envs/`: MJLab environment implementation and environment-side terms.
- `robots/`: Go2 robot metadata and MJCF assets.
- `models/`: configurable MLP actor-critic and network utilities.
- `algos/`: PPO, rollout storage, and advantage estimation.
- `runners/`: train/evaluate orchestration.
- `export/`: TorchScript, ONNX, and metadata export.
- `utils/`: config loading, seeding, logging, checkpointing, and math helpers.

The package should stay implementation-focused. Command-line argument parsing should usually live in `scripts/`.
