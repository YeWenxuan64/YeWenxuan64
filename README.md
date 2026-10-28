# 你好，我是叶文轩 · Hi, I'm YeWenxuan

## 🧬 About Me
- 🏳️‍⚧️ **Trans girl**. sophomore (currently on leave) · a self-proclaimed "full stack engineer".
- ⚡ **Tech** — electrical engineering, hardware and software, computer science. Yours truly covers the whole chain, from soldering iron to terminal.
- 🎹 **Art** — electronic music, electronic vocal (Vocaloid), 3D animation, cinematic photography and video production.
- 🍃 **One rule**: if I like it, I build it with my own hands.


## 🛠 Toolbox
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
[![arduino](https://img.shields.io/badge/Arduino_IDE-00979D?style=flat-square&logo=Arduino)](https://www.arduino.cc/)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white)
![RKNN](https://img.shields.io/badge/Rockchip-RKNN-FF6600?style=flat-square)
![QNN](https://img.shields.io/badge/Qualcomm-QNN-325CAC?style=flat-square)

![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![Orbbec](https://img.shields.io/badge/Orbbec-Depth%20Camera-blueviolet?style=flat-square)
![DJI](https://img.shields.io/badge/DJI-Ronin%20%7C%20Focus-000000?style=flat-square)

![Pygame](https://img.shields.io/badge/Pygame-GUI-2E7D32?style=flat-square)


## 🎯 Working In Poecess

**A stereo-vision focus-sensing rangefinder** — perceives scene depth with a depth camera, understands the frame with AI vision models, and automatically drives the gimbal / focus motor for professional-grade focus control.

```
+-------------------+            +----------------------+             +-------------------+
| Orbbec Depth Cam  | - depth -> |     Focus-Finder     | - frames -> |  Edge_Inferencer  |
+-------------------+            |     (Pygame GUI)     | <- tracks - |   RKNN/QNN/ONNX   |
                                 +----------+-----------+             +-------------------+
                                            |
                             +--------------+--------------+
                        (A)  |                             | (B)
                             v                             v
                  +---------------------+       +---------------------+
                  |   DJI focus motor   |       |  DJI Ronin gimbal   |
                  | independent control |       |    + focus motor    |
                  +---------------------+       +---------------------+

  (A) direct USB-CAN, no WiFi - independent focus motor control.
  (B) WiFi-CAN bridge (ESP32 AP <-> STA) - gimbal control, focus motor follows.
  Routes (A) and (B) are alternatives - pick one per run.
```

This project won an award at the **2025 Qualcomm Edge AI Innovation Challenge**. Hardware, firmware, docs, promo film, launch event and tutorials were all done by yours truly, solo — hence the rule: nothing ships until everything is done. So no rushing me, please (whispers).

>🔒 The main project **Focus-Finder**, the **DJI gimbal / focus motor controller**, and a bunch of model deployment repos are still private while I polish them. They will come out when they are ready.

📚 [Project 330 — full project layout and dependency graph](./Project330.md)


## 📮 Find Me

<div align="center">
  
[![bilibili](https://img.shields.io/badge/Bilibili-00A1D6?style=for-the-badge&logo=bilibili&logoColor=fff)](https://space.bilibili.com/332842679)
[![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=fff)](https://t.me/YeWenxuan64)
[![X (Twitter)](https://img.shields.io/badge/X_(Twitter)-000000?style=for-the-badge&logo=x&logoColor=fff)](https://x.com/YeWenxuan256)

</div>


## 📊 Stats

<p align="center">
  <picture align="center" height="180">
    <source 
      srcset="https://github-stats-extended.vercel.app/api?username=YeWenxuan64&include_all_commits=true&count_private=true&theme=dark"
      media="(prefers-color-scheme: dark)"
    />
    <source
      srcset="https://github-stats-extended.vercel.app/api?username=YeWenxuan64&include_all_commits=true&count_private=true"
      media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
    />
    <img height="180" align="center" src="https://github-stats-extended.vercel.app/api?username=YeWenxuan64&include_all_commits=true&count_private=true" alt="YeWenxuan64's GitHub stats" />
  </picture>
  
  <picture align="center" height="180">
    <source 
      srcset="https://github-stats-extended.vercel.app/api/top-langs/?username=YeWenxuan64&layout=compact&theme=dark&hide=markdown"
      media="(prefers-color-scheme: dark)"
    />
    <source
      srcset="https://github-stats-extended.vercel.app/api/top-langs/?username=YeWenxuan64&layout=compact&hide=markdown"
      media="(prefers-color-scheme: light), (prefers-color-scheme: no-preference)"
    />
    <img height="180" align="center" src="https://github-stats-extended.vercel.app/api/top-langs/?username=YeWenxuan64&layout=compact&hide=markdown" alt="YeWenxuan64's GitHub stats" />
  </picture>
</p>


<details>
<summary>🃏 Easter egg </summary>

## 项目编号: YeWenxuan64

## 项目等级: Safe

> [!TIP]
> 项目在满足既定收容条件时表现稳定，异常效应可控。  
> 若收容措施被破坏、睡眠陪护协议未执行或被激怒，项目可能进入短时激越状态。

---

## 特殊收容措施

**YeWenxuan64** 当前被收容于 Site-~~hanlianyi_shelter(villa)-wuhan~~。

项目需要一间专用卧室，规格如下：

| 区域 | 要求 |
|---|---|
| 类型 | 卧室 / 睡眠收容室 |
| 面积 | 不小于 3m × 3m |
| 环境 | 隔音、低照度、有大床 |
| 温度 | 22℃ 至 27℃ |

项目另需一处活动室，规格如下：

| 区域 | 要求 |
|---|---|
| 类型 | 活动室 / 日常行为收容室 |
| 面积 | 不小于 5m × 5m |
| 环境 | 通风良好，配备基础娱乐设施 |
| 温度 | 22℃ 至 27℃ |
| 设备 | 需配备一台可连接 Internet 的电脑 |


在 **YeWenxuan64** 就寝时，需配备一名经过心理评估的值班人员进行安抚与睡眠陪护。  
若人员紧缺，且经 **YeWenxuan64** **明确同意**后，可使用长度不小于 1m 的玩偶作为临时替代物。

若项目出现激越反应，现场人员应优先采取以下措施：

1. 保持冷静，避免强行约束项目；
2. 降低照明强度与抚摸安抚；
3. 撤离非必要人员；
4. 若激越状态持续超过 5 分钟，通知站点心理干预小组。

---

## 描述

**YeWenxuan64** 是一名外观年龄约为 ~~[数据删除]~~ 的人形异常个体，其生理结构与普通人类高度相似，能够正常进食、睡眠与交流。  
项目性格总体温和，在熟悉环境中表现稳定，对日常娱乐、网络浏览及轻度社交活动有明显兴趣。

项目自称为一名跨领域“全栈工程师”，其自我描述涵盖以下方向：

> A "full stack engineer" in electrical engineering, electronic music (and vocal), animation, cinematic photography and video production.

上述自称内容尚未完全通过基金会技术评估，但项目在相关创作活动中表现出较高主动性与持续学习能力。

异常描述：~~[数据删除]~~

仅在少数情况下观察到项目具有主动攻击意图。  
多数异常现象会在项目情绪恢复稳定后自行消失。

---

## 附录

### 附录 A：收容建议

> 建议将 **YeWenxuan64** 的收容重点放在情绪稳定与睡眠质量维护上。  
> 在满足基本收容条件时，项目风险极低，适合长期稳定收容。

### 附录 B：研究员备注

> **YeWenxuan64** 并非传统意义上的高危异常。  
> 其危险性主要来自未被满足的安全感需求，而非主动恶意。  
> 建议后续收容方案中增加心理陪伴、规律作息与有限度的娱乐活动安排。

### 附录 C：联系方式

> **YeWenxuan64** 渴望与别人交流，可通过以下链接找到Ta。<br>
> [Bilibili](https://space.bilibili.com/332842679)<br>
> [Telegram](https://t.me/YeWenxuan)(experimental)<br>
> [X(Twitter)](https://x.com/YeWenxuan256)(experimental)<br>


</details>
