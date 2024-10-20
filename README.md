# Unity-Machine-Learning-Agents Hummingbirds Course Implementation

This repository contains the implementation of the Hummingbirds course by Adam Kelly using Unity's Machine Learning Agents (ML-Agents) version 2.0.1. The project is designed to train an agent to mimic the behavior of a hummingbird in a simulated environment.

## Training Configuration

The training configuration for the Hummingbird agent is defined as follows:

```yaml
behaviors:
  Hummingbird:
    trainer_type: ppo
    hyperparameters:
      batch_size: 1024
      buffer_size: 10240
      learning_rate: 0.0003
      beta: 0.005
      epsilon: 0.2
      lambd: 0.95
      num_epoch: 3
      learning_rate_schedule: linear
    network_settings:
      normalize: false
      hidden_units: 20
      num_layers: 2
      vis_encode_type: simple
    reward_signals:
      extrinsic:
        gamma: 0.99
        strength: 1.0
    keep_checkpoints: 5
    max_steps: 5000000
    time_horizon: 128
    summary_freq: 10000
```

Here are some screenshots taken during the training process:

![Screenshot 2023-12-29 180432](https://github.com/ogozo/Unity-Machine-Learning-Agents/assets/103512246/d671de74-cdde-4923-b7dd-b79c626445cc)

![Screenshot 2023-12-29 180459](https://github.com/ogozo/Unity-Machine-Learning-Agents/assets/103512246/b6230d53-3c08-4a16-93ee-f2e870117928)
