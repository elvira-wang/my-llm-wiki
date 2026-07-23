---
tags: [chitubox, resin-slicer]
source:
  - "[[3D resin print supports EASY GUIDE]]"
  - "[[How To Get Smooth Surface With Print Angle And Antialiasing]]"
  - "[[光固化支撑老翻车？CHITUBOX这样加支撑，模型表面少留坑！]]"
  - "[[（DLPLCD）光固化3D打印像素纹&抗锯齿详解]]"
  - "[[CHITUBOXの印刷設定を徹底解説！自分でレジンのパラメーター調整ができるようになれば印刷も怖くない？]]"
  - "[[Chitubox 2026 v3.2.0 completo]]"
  - "[[Chitubox Masterclass Resin Printing How To Orient Your 3D Model]]"
  - "[[CHITUBOX V1.3.0 更新日志]]"
  - "[[⚡Nuevo CHITUBOX Guía DEFINITIVA en Español (2026)]]"
  - "[[Tutorial Para INICIANTES no Chitubox Impressão 3D de Resina Elegoo Saturn 3 Ultra]]"
  - "[[ChituBOX! Всё о подготовке к печати и поддержках! Делюсь опытом]]"
  - "[[【光造形3Dプリンター講座】スライスソフトを理解しよう！サポート材、中空処理、スライス設定まで完全解説 【フィギュア製作講座】Chitubox V2.3]]"
  - "[[ПОДДЕРЖКИ, ПЕЧАТЬ, ОБРАБОТКА! У вас легко получится. 2 часть (Печать)]]"
created: 2026-07-14
domain:
  - slicing-software
  - resin-printing
confidence: consensus
knowledge_type: consensus
---

# CHITUBOX

光固化 3D 打印领域使用最广泛的切片软件之一。覆盖从模型导入、预处理、支撑生成到切片输出的完整工作流。有免费版（Basic）、Advanced、Pro、Team 四个版本——"免费版对我来说足够用了"（Dream Reich [^7]；柚P 同样只用免费版 [^6]）。

---

## 工作流覆盖

CHITUBOX 覆盖的工作流按知识链组织如下。每条链中的条目可独立阅读，也可按箭头顺序走通完整流程。

### 模型前处理流

> **[[print-orientation-resin|角度]]**（最上游决策）→ **[[island-detection|孤岛检测]]** + **[[support-structures-resin|支撑]]**（后果与解决）→ **[[hollowing|镂空]]** + **[[drain-holes|排液孔]]**（消除 **[[suction-cup-effect|吸盘]]**）

v1.3.0 新增：[[free-cutting|自由切割]] + [[model-alignment|模型对齐]] + 模型封装（保护盒）。Blender 补充：[[blender-stl-cutting|Blender STL 切割]]（复杂分件 + 连接结构）。

### 工艺参数流

> **[[chitubox-print-settings|参数配置]]** → **[[exposure-calibration|正常曝光校准]]** / **[[bottom-exposure|底层曝光]]** → **[[build-plate-leveling|平台调平]]**

### 表面质量链

> **[[screen-bit-depth|屏幕硬件]]** → **[[pixel-texture|像素纹]]** → **[[anti-aliasing|抗锯齿]]** → **[[grayscale-threshold-testing|灰度阈值测试]]**

### 独立条目

[[post-processing-resin|后处理]] · [[temperature-control|温度控制]] · [[part-joining-methods|零件连接]] · [[tolerance-and-fit|公差设计]] · [[protective-cage|保护笼]]

### 跨领域条目

[[manifold-geometry|流形几何]]（打印前提——所有模型必须水密） · [[ai-3d-generation|AI 3D 生成]]（AI 图像 → 3D 打印流程） · [[cad-software-comparison|CAD 软件选择]]（建模工具对比） · [[fdm-surface-quality|FDM 表面质量]]（FDM 平滑参数）

### 相关软件工具

- [[blender-stl-cutting|Blender STL 切割]]：Blender 中的进阶切割 + 连接工作流
- [[cad-software-comparison|CAD 软件选择]]：面向 3D 打印的建模软件对比

---

## 版本

| 版本 | 主要变化 |
|---|---|
| v1.7.0 | 早期稳定版。VogMan 2020 年视频中使用此版本。基础孤岛检测（眼睛图标）。[^4] |
| v1.3.0 | 引入自由切割、模型对齐、模型封装、单双栏视图切换、Alt 快捷键提示体系、导入布局模式（居中/保留世界坐标）。首个将模型编辑集成到切片软件内的大版本。[^8] |
| v2.3 | 灰度抗锯齿成熟阶段。柚P 2025 年视频中使用的版本。[^6] 移除旧版 Infill 设置项。 |
| v3.2.0 | 2026 年最新版。Dream Reich 以此版本录制完整教程。[^7] |

---

## 切片格式

| 格式 | 用途 | 说明 |
|---|---|---|
| `.cbddlp` | 早期 DLP 格式 | 仅支持闪烁抗锯齿（AA Level），不兼容灰度 AA |
| `.ctb` | 当前主流格式 | 支持灰度抗锯齿。灰度档位压缩至 128（2 个原始档位 → 1 个） |
| `.chitubox` / `.ctp` | 工程文件格式 | 支撑可再次编辑。切片时可区分支撑与模型本体——AA 时支撑不受影响。推荐用于预支撑模型 |

格式选择直接影响 [[anti-aliasing|抗锯齿]] 效果——`.cbddlp` 完全不支持灰度 AA，`.ctb` 的灰度压缩会降低 AA 效果（详见 [[screen-bit-depth|屏幕色深]]）。

---

## 竞品

| 软件 | 特点 |
|---|---|
| **Lychee Slicer** | 社区树脂参数库（Community Profiles）——新手可直接使用已验证的配置，降低入门门槛。VogMan 推荐给绝对新手。[^9] 部分历史版本 AA 存在问题（Dennys Wang 指出 Lychee AA 在某个更新后停止工作 [^2]）。|
| **Elegoo Satelite** | Elegoo 2024 年底推出的免费切片软件。内置部分付费软件才有的功能（如模型切割工具）。仅 Windows。[^10] |

---

## 快捷键（v1.3.0 增强）

| 快捷键 | 功能 |
|---|---|
| `Alt` | 临时显示/隐藏所有快捷键提示 |
| `A` | 添加支撑 |
| `D` | 删除支撑 |
| `E` | 编辑支撑 |
| `Enter` | 确认操作（切割、参数输入） |
| `Esc` | 取消操作 |
| `Shift` + 方向键 | 精确平移视图 |
| 数字键 | 切换布局模式 / 调整镜像方向 |
| `W` / `R` / `E` | 移动 / 旋转 / 缩放（需在设置中自定义 [^6]） |

---

[^1]: Dennys Wang, "My Support Setting - Masterclass Resin Support (MRP) 1" (2023).
[^2]: Dennys Wang, "How To Get Smooth Surface With Print Angle And Antialiasing" (2021).
[^3]: Dennys Wang, "Chitubox Masterclass: How To Orient Your 3D Model" (2023).
[^4]: VogMan, "3D resin print supports EASY GUIDE" (2020).
[^5]: 阿文菌, "光固化支撑老翻车？CHITUBOX这样加支撑" (2026).
[^6]: 柚P, "CHITUBOXの印刷設定を徹底解説" (2023). CHITUBOX 免费版 + 日本语环境。
[^7]: Dream Reich 3D, "Chitubox 2026 v3.2.0 completo" (2026). Elegoo Saturn 3 Ultra.
[^8]: CHITUBOX 官方, "V1.3.0 更新日志" (2026).
[^9]: VogMan, "3D Resin Printing ABSOLUTE BEGINNERS guide" (2024).
[^10]: Uncle Jessy, "Elegoo's new FREE Slicer" (2024).
