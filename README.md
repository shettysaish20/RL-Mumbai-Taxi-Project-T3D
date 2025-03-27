# RL-Mumbai-Taxi-Project-TD3

An extension of my previous iteration of Reinforcement Learning, this model is trained using Twin-Delayed Deep Deterministic Policy Gradient (TD3) to enable a Mumbai Taxi to navigate the streets of Mumbai.

![RL Agent](images/running_image.png)

## Overview

This project implements a Twin-Delayed Deep Deterministic Policy Gradient (TD3) model to train a virtual taxi to drive within a simulated Mumbai environment. The taxi learns to avoid obstacles and reach designated goals.

## Game

The taxi model (**an Actor Model**) has three locations in the map where it has to drop its passengers, while ensuring it takes the right path to reach each of the three locations one-by-one.
- The Environment (**A Critic Model**) gives a reward to the taxi model based on the area it enters and the path it takes to reach the target location
- The areas other than the roads is the **sand area** where the taxi is not supposed to enter and for which it receives a heavy negative penalty.
- There is also time penalty which keeps incrementing based on the time it takes to reach the target location.
- Reward logic of the Game:
    - **Sand Penalty**:
        If the car is on sand (indicated by the sand matrix value > 0 at the car’s position), the car’s velocity is reduced and an immediate penalty of -2 is applied.
    - **Normal Terrain**:
        When off sand, the car moves faster and starts with a base reward of -0.7. If the car’s distance to the goal decreases compared to the previous update, it earns a high reward (+50); otherwise, a small penalty (-0.3) is added to the current reward.
    - **Boundary Check**:
        If the car goes out of bounds, its position is corrected and a hefty penalty of -10 is applied.
    - **Goal Reaching Logic**:
        When the car comes close enough to the goal (distance < 25), the target position is swapped for the next goal, essentially steering the learning towards reaching multiple locations.

## Key Files

-   [T3D_ai_model.py](T3D_ai_model.py): Contains the TD3 implementation, including the neural network architectures (actor and critic) and learning logic.
-   [map.py](map.py): Implements the game environment, car dynamics, and reward system.
-   [car.kv](car.kv): Defines the Kivy UI elements for the car and environment.
-   [images/](images/): Contains images for the map, car, and other visual elements.

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
