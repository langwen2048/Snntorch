# TS

[English](README.md) | [中文](README_zh.md)

触觉传感器 MuJoCo 仿真环境，提供以下功能：

- 通用触觉传感器模组
    - 接近觉
    - 触觉：切向力、法向力、切向力方向（0~360度，指尖为0）
- 带触觉的灵巧手


## 安装

```bash
pip install mujoco==3.2.3
```

## Mujoco模型

可用的触觉传感器模型：

```bash
# 通用触觉传感器模组
python -m mujoco.viewer --mjcf=./mujoco_model/TSModule.xml

# 带触觉的灵巧手
python -m mujoco.viewer --mjcf=./mujoco_model/DexHand.xml
```

注册的传感器回调函数：

```bash
# windows
TSensor.pyd

# linux
TSensor.so
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
