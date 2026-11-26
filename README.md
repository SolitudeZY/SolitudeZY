# Hi, I'm Solitude_ZY 👋

> **让模型真正跑起来——最好跑在摄像头后面那块巴掌大的板子上。**

智能科学与技术 · 计算机视觉 / 边缘端部署 / 多模态大模型应用

我做的东西大多指向同一件事：**把"看得懂"的模型，塞进"用得起"的设备里。** 从数据准备、训练、量化、拆头，到板端拉流推理和告警上报，这条链路我自己走通，也自己在工地上被它坑过。

---

## 🔭 我在做什么

| 方向 | 具体在折腾什么 |
| --- | --- |
| **边端视觉巡检** | 滑坡、交通锥、防护装备、桥梁裂缝——检测 / 分割 / 跨帧追踪，最后压成 INT8 上 RK3576 |
| **多模态大模型落地** | Qwen-VL 两阶段微调（工程安全场景）、自动标注流水线、切片推理、MQTT 服务化 |
| **Agent 与桌面端应用** | 文档生成、舆情监测、通用桌面 Agent——Electron / Tauri / FastAPI 一条龙 |
| **云-端协同工程化** | 设备管理、固件升级、任务下发，云端和板端怎么把话说清楚 |

---

## 🧩 精选项目

### 边端视觉巡检

| 项目 | 说明 |
| --- | --- |
| [**UAV_cone**](https://github.com/SolitudeZY/UAV_cone) | 无人机视角的交通导改锥桶检测：YOLOv8s-OBB 三分类 + MobileNetV3 候选审核，输出锥桶**移位 / 缺失 / 倒伏**告警 |
| [**landslide-detect**](https://github.com/SolitudeZY/landslide-detect) | 滑坡检测与跨帧追踪，YOLOv8 检测 + 时序投票抑制误报，含 RK3576 端侧部署链路 |
| [**rk3576-edge-platform**](https://github.com/SolitudeZY/rk3576-edge-platform) | 板端平台：RTSP 拉流 → RKNN INT8 推理 → YOLO 拆头后处理 → 推流与预览 |
| [**CrackNet**](https://github.com/SolitudeZY/CrackNet) | 桥梁裂缝语义分割：DeepLab + ResNet101 与 U²-Net 双路线，含裂缝宽度量测 |
| [**PPE_Drone**](https://github.com/SolitudeZY/PPE_Drone) | 无人机视角的防护装备识别，YOLO / RT-DETR 对比 |

### 大模型与 Agent 应用

| 项目 | 说明 |
| --- | --- |
| [**QuickModel**](https://github.com/SolitudeZY/QuickModel) ⭐41 | 通用桌面 Agent：把便宜模型用在日常，把强模型留给硬活 |
| [**OpinionLens**](https://github.com/SolitudeZY/OpinionLens) ⭐38 | 舆见：社媒舆情监测与 AI 报告桌面端（Electron + FastAPI + MediaCrawler） |
| [**qwen_fine_tuning**](https://github.com/SolitudeZY/qwen_fine_tuning) | Qwen-VL 两阶段微调：先 grounding 再结构化 JSON，识别边防护/基坑围挡等违规场景 |
| [**Free-Agent**](https://github.com/SolitudeZY/Free-Agent) | 基于 DeepAgent 的 Web 端文档生成：标书撰写、自动化报表 |
| [**qwen-redetect**](https://github.com/SolitudeZY/qwen-redetect) | Qwen-VL 视频/图像识别复核服务，Go API + 内置 Web 复核台 |

### 平台与工具

| 项目 | 说明 |
| --- | --- |
| [**AIhander**](https://github.com/SolitudeZY/AIhander) | 云-端协同 AI 设备管理平台：cloud 控制台 + agent 固件升级 + Detector 边端检测器 |
| [**Free_Train**](https://github.com/SolitudeZY/Free_Train) | Tauri + Rust 写的本地离线视觉数据预处理工具：抽帧、切图、质检、去重、可追溯导出 |
| [**MTD-ISC**](https://github.com/SolitudeZY/MTD-ISC) | 恶意流量检测平台 |
| [**Detection_Platform**](https://github.com/SolitudeZY/Detection_Platform) | 基于 Django 的检测管理 Web 应用 |
| [**ADCAE**](https://github.com/SolitudeZY/ADCAE) | 非对称深度卷积自编码器复现 |

---

## 🛠 技术栈

**模型与训练**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Ultralytics](https://img.shields.io/badge/Ultralytics_YOLO-111F68?style=flat-square)
![RT-DETR](https://img.shields.io/badge/RT--DETR-4B8BBE?style=flat-square)
![DeepLab](https://img.shields.io/badge/DeepLabv3+-3776AB?style=flat-square)
![U2Net](https://img.shields.io/badge/U%C2%B2--Net-6A5ACD?style=flat-square)

**端侧部署**
![RKNN](https://img.shields.io/badge/RKNN--Toolkit2-0F9D58?style=flat-square)
![RK3576](https://img.shields.io/badge/RK3576-FF6F00?style=flat-square)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white)
![INT8](https://img.shields.io/badge/INT8_Quantization-8E44AD?style=flat-square)
![RTSP](https://img.shields.io/badge/RTSP%20%2F%20MediaMTX-1E88E5?style=flat-square)

**大模型**
![Qwen](https://img.shields.io/badge/Qwen--VL-615CED?style=flat-square)
![LoRA](https://img.shields.io/badge/LoRA%20%2F%20DeepSpeed-FFB000?style=flat-square)
![flash-attn](https://img.shields.io/badge/flash--attn-2E7D32?style=flat-square)

**工程**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Electron](https://img.shields.io/badge/Electron-47848F?style=flat-square&logo=electron&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri-24C8DB?style=flat-square&logo=tauri&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white)

---

## 📊 一点数据

- **24** 个原创仓库，**2** 个项目的星标已经能说明问题（QuickModel **41★**、OpinionLens **38★**）
- **4** 类视觉任务跑通过端侧：检测、分割、OBB、跨帧追踪
- **1** 条完整链路：`数据准备 → 训练 → ONNX → INT8 量化 → 拆头 → RK3576 推理 → 告警上报`

---

## 📫 联系我

- 📧 邮箱：[q2205773452@163.com](mailto:q2205773452@163.com) / [xztszy@gmail.com](mailto:xztszy@gmail.com)
- 💬 想聊：边端视觉部署、YOLO 后处理、VLM 微调、或者你也在这条链路上被坑过

![My GitHub Game](game.gif)

**Only by remaining humble can we reach the top of the mountain.**
