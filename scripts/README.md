# Scripts

This directory should contain thin command-line entrypoints.

Expected future files:

- `train.py`: parse arguments, load configs, and call `go2_mjlab.runners.train`.
- `eval.py`: parse checkpoint and config paths, then call `go2_mjlab.runners.evaluate`.
- `export_policy.py`: load a checkpoint and call `go2_mjlab.export`.
- `play.py`: run an interactive or rendered rollout for visual inspection.

Scripts should stay thin. Core logic should live inside the `go2_mjlab/` package so it can be imported and tested.
