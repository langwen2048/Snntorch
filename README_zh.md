# 他山科技触觉模拟仿真平台使用手册

[中文](README_zh.md)

## 一、简介
欢迎使用他山科技触觉模拟仿真平台！本平台基于 MuJoCo 开发，旨在为研究人员和开发者提供一个高效、精准的机器人触觉模拟环境，助力机器人触觉感知技术的研究与创新。我们的模型是国内首个基于真实产品的触觉模拟仿真模型，对推动具身智能机器人的发展具有重要意义。

## 二、功能概述
1. 通用触觉传感器模组 ：包括接近觉、触觉（法向力、切向力、切向力方向（切向力方向 1 ~ 360 度，指尖方向为 0））以及原始电容值（7 个原始电容值）的模拟。
2. 带触觉的灵巧手 ：模拟具有触觉感知能力的灵巧手，可用于研究机器人手部的触觉交互与操作。

触觉传感器 MuJoCo 仿真环境，提供以下功能：

- 通用触觉传感器模组
    - 接近觉
    - 触觉：切向力、法向力、切向力方向（0~359度，指尖为0）
- 带触觉的灵巧手


## 安装

```bash
pip install mujoco==3.2.3
```

## Mujoco模型

带触觉传感器模型：

```bash
# 通用触觉传感器模组
python -m mujoco.viewer --mjcf=./mujoco_model/TSModule.xml

# 带触觉的灵巧手
python -m mujoco.viewer --mjcf=./mujoco_model/DexHand.xml
```

注册的传感器回调函数：

```bash
# windows
mjcb_sensor/win/TSensor.pyd

# linux
mjcb_sensor/linux/TSensor.so
```

## 测试场景

通用触觉模组：
```bash
python module_test.py
```

灵巧手五指握抓：
```bash
python dexhand_grab.py
```


## License

Copyright 2025 TaSHan. 基于 Apache License 2.0 授权。
