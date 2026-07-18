<div align="center">

# Project 330

![madewithlove](https://img.shields.io/badge/made_with-%E2%9D%A4-red?style=for-the-badge&labelColor=pink)

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Rockchip%20|%20Qualcomm%20|%20x86-orange)
![DepthCamera](https://img.shields.io/badge/Camera-Orbbec%20Depth-blueviolet)
![GUI](https://img.shields.io/badge/GUI-Pygame-green)
![CV](https://img.shields.io/badge/CV-Computer%20Vision-brightgreen)
![AI](https://img.shields.io/badge/AI-Detect%20|%20Track%20|%20Saliency-ff69b4)
[![RKNN](https://img.shields.io/badge/Rockchip-RKNN-FF6600)](https://github.com/airockchip/rknn-toolkit2)
[![QNN](https://img.shields.io/badge/Qualcomm-QNN-325CAC)](https://www.qualcomm.com/developer/software/qualcomm-ai-engine-direct-sdk)
![Focus](https://img.shields.io/badge/Follow%20Focus-Automatic-success)
![CAN](https://img.shields.io/badge/CAN-1Mbps%20SLCAN-purple)
![DJI](https://img.shields.io/badge/DJI-Ronin%20|%20Focus%20Motor-black)
[![License: MIT](https://img.shields.io/badge/License-MIT-gree.svg)](https://opensource.org/licenses/MIT)
![License](https://img.shields.io/badge/License-Apache%202.0-blue)


Project 330 是一个以 **AI 边缘计算** 与 **嵌入式系统集成** 为核心的个人项目集。

Awards [*2025 Qualcomm-IEIoT-Challenge*](https://qc-ieiot-challenge.aidlux.com/2025) First Prize?

**🎯 核心目标**: 打造一套**从模型训练到边缘端推理部署、再到硬件控制的全链路系统**，实现**双目视觉焦点感知测距仪** —— 即通过深度相机感知场景深度，结合 AI 视觉模型理解画面内容，自动驱动云台/跟焦器完成专业级焦点控制。

</div>

## **📦 项目构成**:
1. [**Focus-Finder**](#focus-finder) (主项目) — 双目视觉焦点感知测距仪，整合深度相机、AI 推理、Pygame GUI 和 CAN 总线硬件控制

2. [**Edge_ModelDeploy**](#edge-modeldeploy) — 模型转换工具链，将 PyTorch/TF 模型量化部署到 Rockchip/Qualcomm NPU

3. [**Edge_Inferencer**](#edge-inferencer) — 三后端统一推理引擎，作为 Focus-Finder 的推理后端

4. [**DJI-Ronin-gimbal-focus-controller**](#dji-ronin-gimbal-focus-controller) — DJI Ronin 稳定器/跟焦器 CAN 控制器，作为 Focus-Finder 的硬件控制后端

5. [**esp32-wifi-can**](#esp32-wifi-can) — ESP32 无线 CAN 桥接器，为 DJI 设备提供无线控制方案

6. [**avtrack_ModelDeploy**](#avtrack-modeldeploy) — 视觉目标跟踪部署 (PyTorch → ONNX → RKNN/QNN)

7. [**nanotrack_v3_ModelDeploy**](#nanotrack-v3-modeldeploy) — 轻量目标跟踪部署 (PyTorch → ONNX → RKNN/QNN)

8. [**retinaface_mobile_ModelDeploy**](#retinaface-mobile-modeldeploy) — 轻量人脸检测部署 (PyTorch → ONNX → RKNN/QNN)

9. [**msi_net_ModelDeploy**](#msi-net-modeldeploy) — 显著性检测部署 (TensorFlow → ONNX → RKNN/QNN)

10. [**yolo11_ModelDeploy**](#yolo11-modeldeploy) — YOLO11 物体检测 & 姿态估计部署 (PyTorch → ONNX → RKNN/QNN)

11. [**yolo26_ModelDeploy**](#yolo26-modeldeploy) — YOLO26 物体检测 & 姿态估计部署 (PyTorch → ONNX → RKNN/QNN)

12. [**rktop**](#rktop) — Rockchip 性能监视工具


## **🔒 项目限制:**<br>
> 本小姐给的限制

![NoCompile(pkg available)](https://img.shields.io/badge/no%20compile%20(pkg%20available)-passing?style=for-the-badge&labelColor=555&color=success)
![NoPCB](https://img.shields.io/badge/no%20pcb-passing?style=for-the-badge&labelColor=555&color=success)
![NoGPIO](https://img.shields.io/badge/no%20gpio-passing?style=for-the-badge&labelColor=555&color=success)
![NoCSIDSI](https://img.shields.io/badge/no%20csi%2Fdsi-passing?style=for-the-badge&labelColor=555&color=success)

![PythonOnly(pkg available)](https://img.shields.io/badge/Python%20only%20(pkg%20available)-passing?style=for-the-badge&labelColor=555&color=blue)
![USBOnly](https://img.shields.io/badge/usb%20only-passing?style=for-the-badge&labelColor=555&color=blue)
![HdmiDpOnly](https://img.shields.io/badge/hdmi%2Fdp%20only-passing?style=for-the-badge&labelColor=555&color=blue)



## **🚀 关于提前(即时)发布仓库:**<br>
由于本项目是叶姐姐**一个人独立**开发的，而且是"**真·全栈开发**"(软/硬件、文档、宣传片、发布会、视频教程等)工作，因此所需要的时间会比预期**长很多**，而且小女子的要求是要**完成全部**工作才发布内容。<br>

再者是因为小女子为了能拿到**高通 QCS6490 的开发板**做适配，而参加了 [*2025高通边缘智能创新应用大赛*](https://qc-ieiot-challenge.aidlux.com/2025) ，并且还拿了奖，所以本小姐**有责任**公布源代码（尽管没有写一定要公布源代码）<br>

还有再者是因为

因此在今年的 [*2026高通具身智能与机器人大赛*](https://qc-ieiot-challenge.aidlux.com/2026/) 的参赛项目书交截止日期 (2026.07.20)，提前发布部分与**高通**强相关的仓库。

本次提前发布的项目是:<br>
- **Edge_ModelDeploy**
- **Edge_Inferencer**
- **yolo26_ModelDeploy** (作为`Edge_ModelDeploy`和`Edge_Inferencer`的例子)
- **esp32-wifi-can**
- **rktop**


**🏆 "2025高通边缘智能创新应用大赛"相关:**<br>
[入围名单(fig.1)](https://blog.csdn.net/aidlux/article/details/151177986)<br>

[奖项公布/领奖/演讲](https://blog.csdn.net/AidLux/article/details/157129510?spm=1001.2014.3001.5502)

["开发者日记"?](https://blog.csdn.net/AidLux/article/details/157399148?spm=1001.2014.3001.5502)

[项目预告视频(BiliBili)](https://www.bilibili.com/video/BV1JBrgBaEzu)

[奖品开箱视频(BiliBili)](https://www.bilibili.com/video/BV1FDzmBwEAX)

---
## 🔗 项目间依赖关系

```
┌──────────────────────────────────────────────┐
│   Focus-Finder                               │
│                                              │
│   ┌──────────────────────────────────────┐   │   ┌───────────────────┐
│   │  DJI-Ronin-gimbal-focus-controller   ├───────▶  esp32-wifi-can  │
│   └──────────────────────────────────────┘   │   └───────────────────┘
│                                              │
│   ┌──────────────────────────────────────┐   │
│   │  Edge_Inferencer                     │   │
│   └────────────────────────────────────▲─┘   │
│                                        │     │
│   ┌─────────────────────────────────┐  │     │
│   │  nanotrack_v3_ModelDeploy       ├──┤     │
│   ├─────────────────────────────────┤  │     │
│   │  avtrack_ModelDeploy            ├──┤     │
│   ├─────────────────────────────────┤  │     │
│   │  retinaface_mobile_ModelDeploy  ├──┤     │
│   ├─────────────────────────────────┤  │     │
│   │  msi_net_ModelDeploy            ├──┤     │
│   ├─────────────────────────────────┤  │     │
│   │  yolo11_ModelDeploy             ├──┤     │
│   ├─────────────────────────────────┤  │     │
│   │  yolo26_ModelDeploy             ├──┤     │
│   └─────────────────────────────────┘  │     │
│                                        │     │
└────────────────────────────────────────│─────┘
                                         │
┌────────────────────────────────────────▼─────┐
│   Edge_ModelDeploy                           │
│                                              │
└──────────────────────────────────────────────┘

┌──────────────────────────────────────────────┐
│   rktop                                      │
│                                              │
└──────────────────────────────────────────────┘

```

```
Git 子模块关系 (Focus-Finder 内部):

  Focus-Finder/
  ├── Programs/AI/Edge_Inferencer/    ──> github.com/YeWenxuan64/Edge_Inferencer
  │                                        (统一推理后端: RKNN/QNN/ONNX)
  │
  ├── Programs/Focus/                 ──> github.com/YeWenxuan64/DJI-Ronin-gimbal-focus-controller
  │                                        (DJI 稳定器/跟焦器 CAN 控制器)
  │
  └── docs/performance_turning/rktop/ ──> github.com/YeWenxuan64/rktop
                                           (Rockchip NPU 性能监视工具)

  独立项目引用:
  ── esp32-wifi-can          (WiFi-CAN 桥接固件, 硬件依赖)
  ── Edge_ModelDeploy        (模型转换工具链, 开发依赖)
```


---
<a id="focus-finder"></a>
## 🎥 Focus-Finder  (主项目 — 双目视觉焦点感知测距仪)

[github.com/YeWenxuan64/Focus-Finder](https://github.com/YeWenxuan64/Focus-Finder)

**简介**: 通过 Orbbec 深度相机获取深度数据，结合 AI 模型进行目标检测/跟踪/显著性分析，自动计算焦平面和景深，通过 CAN 总线控制 DJI Ronin 稳定器/跟焦电机实现自动跟焦。运行于 Rockchip NPU / Qualcomm HTP / x86 平台。

```
Focus-Finder/
├── Programs/
│   ├── *.py
│   ├── config/
│   ├── fonts/
│   ├── pictures/
│   ├── test/
│   ├── legacy/
│   ├── AI/
│   │   ├── Edge_Inferencer/  统一推理后端 (RKNN/QNN) (git submodule)
│   │   ├── yolo/             YOLO11/YOLO26 物体检测 & 姿态估计
│   │   ├── nanotrack/        NanoTrackV3 轻量目标跟踪
│   │   ├── avtrack/          AVTrack 视觉目标跟踪 (ICML 2024)
│   │   ├── retinaface/       RetinaFace-mobile 人脸检测
│   │   └── msi_net/          MSI-Net 显著性检测
│   └── Focus/                DJI 稳定器/跟焦器 CAN 控制器 (git submodule)
│
├── docs/
│   ├── Menu_Introduction.md
│   ├── install_rules/
│   ├── system_scripts/
│   └── performance_turning/
│       ├── rktop/            Rockchip 性能监视工具 (git submodule)
│       └── *_hight_performance.sh
│
└── requirements.txt
```

**依赖关系**:
- 推理后端 → `Edge_Inferencer` (git submodule, 统一 RKNN/QNN/ONNX)
- 硬件控制 → `DJI-Ronin-gimbal-focus-controller` (git submodule)
- 无线 CAN → `esp32-wifi-can` (独立项目, WiFi-CAN 桥接固件)
- 模型转换 → `Edge_ModelDeploy` (独立项目, 量化部署工具链)
- 性能监视 → `rktop` (git submodule, Rockchip 性能监视工具)


---
<a id="dji-ronin-gimbal-focus-controller"></a>
## 🎮 DJI-Ronin-gimbal-focus-controller (子项目 — DJI Ronin 云台/焦点控制器)

[github.com/YeWenxuan64/DJI-Ronin-gimbal-focus-controller](https://github.com/YeWenxuan64/DJI-Ronin-gimbal-focus-controller)

**简介**: 通过 CAN 总线控制大疆如影（Ronin）系列稳定器以及**独立控制**跟焦电机的统一 Python 接口库。<br>
作为 Focus-Finder 的硬件控制子模块被引用。

```
DJI-Ronin-gimbal-focus-controller/
├── focus_controller.py              多进程控制器主入口 
├── dji_ronin_controller.py          稳定器 CAN 协议实现 
├── dji_res_eng_controller.py        逆向跟焦器 CAN 协议实现 
├── focus_utilities.py
├── documents_and_images/
└── legacy/
```


---
<a id="esp32-wifi-can"></a>
## 📡 esp32-wifi-can  (子项目 — ESP32 无线 SLCAN 总线桥接器)

[github.com/YeWenxuan64/esp32-wifi-can](https://github.com/YeWenxuan64/esp32-wifi-can)

**简介**: 基于 ESP32 系列 (C3/C6/S3) 的 WiFi-CAN 透明桥接 Arduino 固件。支持 LAWICEL/SLCAN 协议，通过 UDP 将 CAN 总线无线延伸。<br>
为 Focus-Finder 的 DJI 设备控制提供无线连接方案。

```
esp32-wifi-can/
├── esp32_wifi_ap/         AP 模式: USB 串口 ⇄ WiFi UDP 桥接 (连接上位机)
├── esp32_wifi_sta_twai/   STA 模式: WiFi UDP ⇄ TWAI CAN 网关 (连接 CAN 总线)
├── legacy/
├── images/
├── README.md
└── LICENSE

数据流: Host → USB → ESP32 AP [UDP] → ESP32 STA [TWAI CAN] → CAN Bus
```


---
<a id="edge-modeldeploy"></a>
## 📦 Edge_ModelDeploy  (子项目 — 边缘模型部署器)

[github.com/YeWenxuan64/Edge_ModelDeploy](https://github.com/YeWenxuan64/Edge_ModelDeploy)

**简介**: 可复用的模型转换工具链。支持 PyTorch/TensorFlow 模型统一转换为 ONNX，再量化部署到 Rockchip NPU (RKNN) 或 Qualcomm HTP (QNN) 边缘设备。<br>
为 Focus-Finder 提供模型转换支持。

```
Edge_ModelDeploy/
├── utilities/                       核心转换工具链
│   ├── onnx_to_rknn.py              ONNX → RKNN (Rockchip NPU)
│   ├── onnx_to_qnn.py               ONNX → QNN (Qualcomm HTP)
│   ├── qnn_accuracy_debugger.py     QNN 精度调试
│   └── yolo_cropped_dataset_gen.py  量化校准数据集生成
│
├── Edge_Inferencer/                 统一推理后端 (独立可复用)
├── avtrack_ModelDeploy/             视觉目标跟踪 (ICML 2024)   (git submodule)
├── nanotrack_v3_ModelDeploy/        轻量目标跟踪 (NanoTrack)   (git submodule)
├── retinaface_mobile_ModelDeploy/   轻量人脸检测 (RetinaFace)  (git submodule)
├── msi_net_ModelDeploy/             显著性检测 (MSI-Net)       (git submodule)
├── yolo11_ModelDeploy/              YOLO11 物体检测 & 姿态估计 (git submodule)
├── yolo26_ModelDeploy/              YOLO26 物体检测 & 姿态估计 (git submodule)
│
├── datasets/                        量化校准数据集 (COCO/WIDER/ImageNet 子集)
├── legacy/
└── requirements_*.txt
```


---
<a id="edge-inferencer"></a>
## ⚡ Edge_Inferencer  (子项目 — 统一边缘推理后端)

[github.com/YeWenxuan64/Edge_Inferencer](https://github.com/YeWenxuan64/Edge_Inferencer)

**简介**: 统一的边缘设备推理引擎，一套 Python API 自动适配 Rockchip NPU (RKNN)、Qualcomm HTP (QNN) 和 ONNX Runtime (CPU)。根据模型文件后缀自动选择推理后端，无需修改业务代码即可在不同硬件间无缝迁移。<br>
作为 Focus-Finder 的推理后端被引用。

```
Edge_Inferencer/
├── ai_inferencer.py        统一入口 AIInferencer (自动识别 .rknn / .bin / .onnx)
├── rknn_inferencer.py      Rockchip NPU 推理后端 (Executor / ThreadPool)
├── qnn_inferencer.py       Qualcomm HTP 推理后端 (Executor / ProcessPool / TaskPool)
├── onnx_inferencer.py      ONNX Runtime CPU 推理后端
├── README.md
├── PERFORMANCE.md
├── QNN_INSTALL.md
├── images/
├── requirements_*.txt
└── LICENSE
```


---
## 🤖 AI模型部署

各模型模块依赖 `Edge_ModelDeploy`，作为独立仓库维护，提供 PyTorch/TensorFlow → ONNX → RKNN/QNN 的全链路转换脚本。

<a id="avtrack-modeldeploy"></a>
### avtrack_ModelDeploy — 视觉目标跟踪

[github.com/YeWenxuan64/avtrack_ModelDeploy](https://github.com/YeWenxuan64/avtrack_ModelDeploy)

将 [AVTrack](https://github.com/wuyou3474/AVTrack)（ICML 2024）目标跟踪模型从 PyTorch 转换为 ONNX，再量化部署到 Rockchip NPU / Qualcomm HTP。输出目标边界框，适用于 UAV 跟踪等实时场景。

<a id="nanotrack-v3-modeldeploy"></a>
### nanotrack_v3_ModelDeploy — 轻量目标跟踪

[github.com/YeWenxuan64/nanotrack_v3_ModelDeploy](https://github.com/YeWenxuan64/nanotrack_v3_ModelDeploy)

NanoTrackV3 轻量级目标跟踪模型部署。采用双分支 Siamese 网络结构（模板分支 + 搜索分支），输出目标得分图和边界框，专为边缘端实时跟踪优化。

<a id="retinaface-mobile-modeldeploy"></a>
### retinaface_mobile_ModelDeploy — 轻量人脸检测

[github.com/YeWenxuan64/retinaface_mobile_ModelDeploy](https://github.com/YeWenxuan64/retinaface_mobile_ModelDeploy)

将 RetinaFace-mobile（MobileNet0.25 骨干）人脸检测模型从 PyTorch 转换部署到边缘端 NPU。同时输出人脸边界框和 5 点关键点（双眼、鼻尖、嘴角），模型仅 ~1.7MB。

<a id="msi-net-modeldeploy"></a>
### msi_net_ModelDeploy — 显著性检测

[github.com/YeWenxuan64/msi_net_ModelDeploy](https://github.com/YeWenxuan64/msi_net_ModelDeploy)

将 MSI-Net 显著性检测模型从 TensorFlow SavedModel 转换部署到边缘端 NPU。输出像素级显著性热力图，倾向于识别人脸、高饱和颜色和复杂纹理区域，与目标检测模型互补使用。

<a id="yolo11-modeldeploy"></a>
### yolo11_ModelDeploy — 物体检测 & 姿态估计

[github.com/YeWenxuan64/yolo11_ModelDeploy](https://github.com/YeWenxuan64/yolo11_ModelDeploy)

基于 Ultralytics YOLO11 框架，支持目标检测（COCO 80 类）和姿态估计（COCO 17 关键点）双任务。选用 s 级小模型，从 PyTorch 经 ONNX 量化部署到 Rockchip / Qualcomm NPU。

<a id="yolo26-modeldeploy"></a>
### yolo26_ModelDeploy — 物体检测 & 姿态估计

[github.com/YeWenxuan64/yolo26_ModelDeploy](https://github.com/YeWenxuan64/yolo26_ModelDeploy)

基于 Ultralytics YOLO26 框架，支持目标检测（COCO 80 类）和姿态估计（COCO 17 关键点）双任务。选用 s 级小模型，从 PyTorch 经 ONNX 量化部署到 Rockchip / Qualcomm NPU。


---
<a id="rktop"></a>
## 🖥️ rktop  (子项目 — Rockchip NPU 性能监视工具)

[github.com/YeWenxuan64/rktop](https://github.com/YeWenxuan64/rktop)

**简介**: Rockchip NPU 性能实时监视工具。一个轻量级的 bash 脚本，实时显示 NPU 利用率、频率、温度等关键指标。<br>
作为 Focus-Finder 的性能调优辅助工具被引用。

```

