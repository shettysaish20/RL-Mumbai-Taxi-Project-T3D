# RL-Mumbai-Taxi-Project-T3D

An extension of my previous iteration of Reinforcement Learning, this model is trained using Twin-Delayed Deep Deterministic Policy Gradient (TD3) to enable a Mumbai Taxi to navigate the streets of Mumbai.

![RL Agent](images/running_image.png)

## Overview

This project implements a Twin-Delayed Deep Deterministic Policy Gradient (TD3) model to train a virtual taxi to drive within a simulated Mumbai environment. The taxi learns to avoid obstacles and reach designated goals.

## Key Files

-   [T3D_ai_model.py](RL-Mumbai-Taxi-Project-T3D/T3D_ai_model.py): Contains the TD3 implementation, including the neural network architectures (actor and critic) and learning logic.
-   [map.py](RL-Mumbai-Taxi-Project-T3D/map.py): Implements the game environment, car dynamics, and reward system.
-   [car.kv](RL-Mumbai-Taxi-Project-T3D/car.kv): Defines the Kivy UI elements for the car and environment.
-   [images/](RL-Mumbai-Taxi-Project-T3D/images/): Contains images for the map, car, and other visual elements.

## Dependencies

-   numpy
-   matplotlib
-   kivy
-   PIL (Pillow)
-   torch

## Usage

1.  Install the dependencies.
2.  Run `map.py` to start the simulation.

```sh
python map.py
```
