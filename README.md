# Robotics Project: Autosub6000 AUV & AURORA Dataset Analysis

This repository contains robotics algorithms and simulation models developed for autonomous underwater vehicle (AUV) navigation, kinematics, dynamics, control, and perception based on the Autosub6000 platform and the AURORA dataset.

## Repository Contents

| File | Description |
|---|---|
| [`forward_kin.py`](forward_kin.py) | **Forward Kinematics**: Implements $\dot{\eta} = J(\eta) \cdot \nu$ transforming body velocities (DVL/IMU) into earth-fixed coordinates. |
| [`inv_kinematic.py`](inv_kinematic.py) | **Inverse Kinematics**: Computes required body-frame velocities $\nu = J(\eta)^{-1} \cdot \dot{\eta}_{\text{desired}}$ to follow desired waypoint trajectories. |
| [`forward_dynamics.py`](forward_dynamics.py) | **Forward Dynamics**: Simulates AUV motion under applied forces and moments using equations of motion (added mass, Coriolis, damping, buoyancy). |
| [`inv_dynamics.py`](inv_dynamics.py) | **Inverse Dynamics**: Determines required thrust, forces, and moments to achieve target accelerations and velocities. |
| [`pid_controller.py`](pid_controller.py) | **PID Controller**: Closed-loop control system for depth, pitch, and heading regulation. |
| [`a_planning.py`](a_planning.py) | **A\* Path Planning**: Grid-based path planning for collision-free navigation across traversable terrain. |
| [`cnn.py`](cnn.py) | **CNN Model**: Convolutional neural network pipeline utilizing AURORA dataset imagery for perception and classification tasks. |

## Prerequisites

Python 3.8+ with the following packages:
- `numpy`
- `matplotlib`
- `scipy` (if applicable)
- `torch` / `torchvision` (for CNN)

```bash
pip install numpy matplotlib scipy torch torchvision
```

## Usage

Run any individual module directly with Python:

```bash
python forward_kin.py
python inv_kinematic.py
python forward_dynamics.py
python inv_dynamics.py
python pid_controller.py
python a_planning.py
python cnn.py
```
