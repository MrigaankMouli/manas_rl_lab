# Utilities

This directory should contain shared helper code.

Expected future files:

- `config.py`: load and merge YAML configs, validate required fields, and expose typed config objects if desired.
- `seeding.py`: set Python, NumPy, Torch, and simulator seeds.
- `logging.py`: metric logging, scalar summaries, and run directory creation.
- `checkpoints.py`: save and load model, optimizer, normalizer, and training state.
- `math.py`: quaternion, rotation, clipping, scaling, and tensor math helpers used across env and training code.

