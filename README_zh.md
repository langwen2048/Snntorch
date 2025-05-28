# 他山科技触觉模拟仿真平台使用手册

[中文](README_zh.md)

## 一、简介
欢迎使用他山科技触觉模拟仿真平台！本平台基于 MuJoCo 开发，旨在为研究人员和开发者提供一个高效、精准的机器人触觉模拟环境，助力机器人触觉感知技术的研究与创新。我们的模型是国内首个基于真实产品的触觉模拟仿真模型，对推动具身智能机器人的发展具有重要意义。

## 二、功能概述
- 通用触觉传感器模组 ：包括接近觉、触觉（法向力、切向力、切向力方向（切向力方向 1 ~ 360 度，指尖方向为 0））以及原始电容值（7 个原始电容值）的模拟。
- 带触觉的灵巧手 ：模拟具有触觉感知能力的灵巧手，可用于研究机器人手部的触觉交互与操作。

## 三、安装指南
1. 安装：在开始使用本平台之前，请确保您的系统满足以下要求并按照步骤进行安装。
- 环境要求
  -- 操作系统：Windows 或 Linux
  -- Python 版本：3.8 或以上


- python环境MuJoCo安装
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
