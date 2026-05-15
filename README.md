# DQN Toy Capacitor Switching

This repository contains a toy reinforcement learning demo for capacitor switching control in a simple radial distribution network.

The environment is built with `pandapower` and follows the Gymnasium-style `reset()` / `step()` interface. A DQN agent is trained to control a switchable capacitor bank according to load and voltage conditions.

## Contents

- `grid/DQN_ToyCapacitorSwitching.ipynb`: main notebook
- `requirements-grid.txt`: required Python packages

## Main features

- Three-bus toy distribution network
- Switchable capacitor bank at the terminal bus
- DQN agent with replay buffer and target network
- Baseline comparison:
  - random policy
  - always-off policy
  - always-on policy
  - hysteresis rule policy
- Paired episode comparison
- Action and transition diagnostics
- Single-episode rollout visualization

## Notes

This is a small educational demo. In this three-bus system, the rule-based hysteresis policy is already very competitive. The main goal is to validate the DQN + pandapower workflow before moving to larger standard distribution test feeders.
