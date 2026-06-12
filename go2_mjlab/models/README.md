# Models

This directory should contain neural network modules.

The intended architecture is a simple actor-critic:

- actor: MLP from observation vector to action mean
- critic: MLP from observation vector to scalar value
- configurable hidden dimensions for both actor and critic
- configurable activation function
- Gaussian action distribution with configurable or learned standard deviation

Expected future files:

- `mlp.py`: reusable MLP builder from input dimension, hidden dimensions, output dimension, and activation name.
- `actor_critic.py`: main policy module with `act`, `act_inference`, `evaluate_actions`, and value prediction methods.
- `distributions.py`: Gaussian policy helpers if distribution logic becomes large enough to separate.
- `normalizer.py`: optional running observation normalization.

Do not place environment logic here. Models should consume tensors and return tensors.
