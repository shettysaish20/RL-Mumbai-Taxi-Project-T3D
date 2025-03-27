# RL-Mumbai-Taxi-Project
A Reinforcement Learning model trained to empower the Mumbai Taxi learn to navigate the bustling streets of Mumbai


![RL Agent](images/running_image.png)

## Overview

This project implements a Deep Q-Network (DQN) to train a virtual taxi to drive within a simulated Mumbai environment. The taxi learns to avoid sand (obstacles) and reach designated goals.

## Key Files

-   [ai.py](RL-Mumbai-Taxi-Project/ai.py): Contains the DQN implementation, including the neural network architecture and learning logic.
-   [map.py](RL-Mumbai-Taxi-Project/map.py): Implements the game environment, car dynamics, and reward system.
-   [car.kv](RL-Mumbai-Taxi-Project/car.kv): Defines the Kivy UI elements for the car and environment.
-   [images/](RL-Mumbai-Taxi-Project/images/): Contains images for the map, car, and other visual elements.

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