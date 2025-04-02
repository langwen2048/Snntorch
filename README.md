# TS

[English](README.md) | [中文](README_zh.md)

The MuJoCo simulation environment for haptic sensors provides the following features:

- General tactile sensor module
    - Proximity Sensing
    - Tactile: tangential force, normal force, direction of tangential force (0-359 degrees, with the fingertip at 0)
- A dexterous hand with haptics


## Installation

```bash
pip install mujoco==3.2.3
```

## Mujoco Models

Model with tactile sensor:

```bash
# General tactile sensor module
python -m mujoco.viewer --mjcf=./mujoco_model/TSModule.xml

# Tactile dexterous hand
python -m mujoco.viewer --mjcf=./mujoco_model/DexHand.xml
```

Registered sensor callback function:

```bash
# windows
mjcb_sensor/win/TSensor.pyd

# linux
mjcb_sensor/linux/TSensor.so
```

## Test Scenario

General tactile module:
```bash
python module_test.py
```

Dexterous hand five fingers grasp:
```bash
python dexhand_grab.py
```


## License

Copyright 2025 TASHan. Licensed under the Apache License, Version 2.0.
