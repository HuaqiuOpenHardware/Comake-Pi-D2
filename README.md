<h1 align="center">Comake Pi D2</h1>

<p align="center"><strong>基于 SigmaStar SSC309QL 的低功耗端侧 AI 开发板</strong></p>

<p align="center">
  <a href="README_EN.md">English</a> |
  <strong>简体中文</strong>
</p>

<p align="center">
  <a href="https://p.eda.cn/d-1377570469779079168">原始项目</a> ·
  <a href="https://doc.comake.online/d2_sigdoc_zh/customer/IPC/EnvironmentSetup/get_started_zh.html">官方文档</a> ·
  <a href="hardware/pcb/">硬件设计</a> ·
  <a href="hardware/bom/">BOM</a> ·
  <a href="docs/">文档资料</a>
</p>

<p align="center">
  🛠️ <a href="https://github.com/HuaqiuOpenHardware/Comake-Pi-D2/issues/new">提交问题</a>
  &nbsp;·&nbsp;
  ⭐ <a href="https://github.com/HuaqiuOpenHardware/Comake-Pi-D2">收藏项目</a>
  &nbsp;·&nbsp;
  🤝 <a href="#参与项目">参与项目</a>
</p>

![Comake Pi D2 端侧 AI 开发板](assets/images/cover.png)

Comake Pi D2 是星宸科技（SigmaStar）面向便携相机、AI 穿戴设备、智能家居和无人机等场景推出的轻量级端侧 AI 开发板。本仓库整理并开放 V1.0 / V2.0 硬件设计包、核心板与载板资料、BOM、硬件说明和 SSC309QL 相关文档，方便开发者检索、复刻与二次开发。

> 本仓库同时包含多个硬件版本。开始设计或打样前，请先确认 V1.0 / V2.0、核心板 / 载板及具体音频配置，不要混用不同版本的原理图、PCB、BOM 和说明文档。

## 一眼看懂

| 项目 | 内容 |
| --- | --- |
| 主控平台 | SigmaStar SSC309QL |
| CPU | 双核 Arm Cortex-A32，最高 1 GHz；200 MHz Cortex-M4 协处理器 |
| AI 加速 | 1.5 TOPS NPU（来自原项目页与官方资料） |
| 内存 | 256 MB LPDDR4x |
| 系统 | Linux / Alkaid SDK 生态 |
| 典型接口 | MIPI RX、UART、I2C、SPI、PWM、SAR ADC、USB 2.0、eMMC / SDIO、RTC |
| 硬件资产 | V1.0 / V2.0 设计包、核心板、载板、BOM、PCB、原理图与硬件说明 |
| 典型场景 | AI 眼镜、便携相机、智能门锁/门铃、宠物机器人、FPV 无人机 |

参数用于资料导航，不代表本仓库维护者完成了独立硬件实测。功耗、AI 性能、摄像头能力和接口兼容性请以对应硬件版本、官方文档及实际验证结果为准。

## 版本与资料选择

| 版本/资料 | 推荐入口 | 说明 |
| --- | --- | --- |
| V1.0 Demo | [`Comake-Pi-D2-V1.0_BGA8_9.5_Demo_20251215.zip`](hardware/pcb/Comake-Pi-D2-V1.0_BGA8_9.5_Demo_20251215.zip) | V1.0 设计包及解压资料 |
| V2.0 完整 Demo | [`Comake-Pi-D2-V2.0_BGA8_9.5_Demo_20260409.zip`](hardware/pcb/Comake-Pi-D2-V2.0_BGA8_9.5_Demo_20260409.zip) | V2.0 核心板、载板和硬件说明的整包入口 |
| V2.0 核心板 | [`Comake-Pi-D2-V2.0_核心板.zip`](hardware/pcb/Comake-Pi-D2-V2.0_核心板.zip) | 单独查看核心板资料 |
| V2.0 载板 | [`Comake-Pi-D2-V2.0_载板.zip`](hardware/pcb/Comake-Pi-D2-V2.0_载板.zip) | 单独查看载板资料 |
| BOM | [`hardware/bom/`](hardware/bom/) | D2 与 Mainboard 元件清单 |
| SSC309QL 用户指南 | [`SSC309QL_HW_USER_GUIDE_20251225.pdf`](docs/SSC309QL_HW_USER_GUIDE_20251225.pdf) | 芯片硬件参考资料 |
| 资料阅读指南 | [`资料阅读指南V1.1.pdf`](docs/资料阅读指南V1.1.pdf) | 建议优先阅读 |
| 文件来源与校验 | [`MANIFEST.json`](MANIFEST.json) | 原始附件来源、大小与 SHA256 |

官方资料说明 V2.0 存在不同音频通路配置。涉及 TWS、WQ7036AX、SSC309QL 音频通路或相关器件时，应结合具体板卡版本、BOM 和硬件说明确认，不能仅根据“V2.0”名称判断。

## 快速开始

### 1. 先确认目标

- 只想了解平台：先看[官方快速开始](https://doc.comake.online/d2_sigdoc_zh/customer/IPC/EnvironmentSetup/get_started_zh.html)。
- 准备复刻整板：从 V2.0 完整 Demo 包和资料阅读指南开始。
- 只修改核心板或载板：使用对应的独立设计包，不要从其他版本拼接文件。
- 准备采购和贴片：同时核对 BOM、PCB、原理图、位号图和实物版本。

### 2. 阅读硬件资料

仓库同时保存原始 ZIP 和便于在线浏览的解压文件。原始包用于来源校验，解压目录用于快速查看；两者内容重复属于归档设计，不代表存在两个不同硬件版本。

### 3. 设计与打样前检查

1. 确认目标板卡版本和音频配置。
2. 核对原理图、PCB、BOM、位号图和 IO 分配表是否属于同一版本。
3. 检查替代料、连接器方向、电源、启动配置、高速接口和射频相关设计。
4. 使用对应 EDA 工具重新执行设计检查，并重新生成制造文件。
5. 对任何修改版明确标记“已审阅”“已打样”或“已实测”，不要把推断写成测试结论。

## 仓库结构

```text
.
├── assets/images/        # 项目封面与社区图片
├── docs/                 # SSC309QL 用户指南、资料阅读指南
├── enclosure/            # 结构件资料状态说明
├── hardware/
│   ├── bom/              # D2 与 Mainboard BOM
│   └── pcb/              # V1.0 / V2.0 设计包及解压文件
├── MANIFEST.json         # 原始附件来源、大小与 SHA256
├── REVIEW_CHECKLIST.md   # 发布前检查记录
├── README.md
└── README_EN.md
```

## 许可证与使用边界

华秋开源硬件社区原项目页的许可证字段标注为 **GPL 3.0**。仓库内同时包含硬件设计文件、芯片文档、Office/PDF 资料和其他上游材料，这些文件可能保留各自的版权或使用条款。

在复制、修改、制造、再分发或商用前：

- 保留原文件中的版权、商标和许可证声明；
- 检查设计包和文档中的独立授权说明；
- 不要仅凭仓库首页的 GPL 3.0 标签推定所有第三方资料采用相同许可；
- 对授权范围不明确的材料，先向原项目方或权利人确认。

## 参与项目

- 报告资料缺失或链接问题时，请注明具体路径和硬件版本。
- 报告硬件问题时，请附板卡版本、供电、外围连接、测量结果和复现步骤。
- 提交设计修改时，请说明影响的 PCB、BOM、接口、版本和验证状态。
- 不要在 Issue 中公开 Wi-Fi 密码、设备密钥、量产凭据或其他敏感信息。

## 获取帮助与加入交流

需要查找 Comake Pi D2 资料、确认硬件版本、加入开源硬件交流群或反馈仓库问题，可以添加 **华秋开源硬件小助手**。

<p align="center">
  <img src="assets/images/wechat-assistant-qr.png" width="220" alt="华秋开源硬件小助手微信二维码">
</p>

<p align="center"><strong>微信扫码添加小助手</strong></p>

<p align="center">添加时建议备注“Comake Pi D2”，方便更快对接相关资料与交流群。</p>

## 来源与检索词

- 原始项目：[星宸科技 AI 开发板 Comake Pi D2](https://p.eda.cn/d-1377570469779079168)
- 官方文档：[Comake Pi D2 快速开始](https://doc.comake.online/d2_sigdoc_zh/customer/IPC/EnvironmentSetup/get_started_zh.html)

相关名称：Comake Pi D2、SigmaStar、星宸科技、SSC309QL、WQ7036AX、edge AI、AI development board、AI glasses、embedded Linux、NPU、hardware design、PCB、schematic、BOM。
