---
tags: [chitubox/workflow, resin-slicer/workflow]
source:
  - "[[3D resin print supports EASY GUIDE]]"
  - "[[How To Get Smooth Surface With Print Angle And Antialiasing]]"
  - "[[Chitubox Masterclass Resin Printing How To Orient Your 3D Model]]"
  - "[[The Perfect Angle of 3D Printing Resin  Chitubox Tutorial]]"
  - "[[How to Perfectly Orient Your 3D Model  Lychee Slicer Tutorial]]"
created: 2026-07-14
domain:
  - resin-printing
  - slicing-software
solves: [[suction-cup-effect]]
confidence: consensus
knowledge_type: consensus
---

# 打印角度 (Print Orientation)

## 定义

模型在构建平台上相对于水平面的摆放角度。光固化打印中，这是**最上游的决策**——摆放角度直接决定了后续所有操作的量和难度。

**前置知识**：理解光固化打印机倒置打印机制（平台悬挂于料槽上方，逐层从 FEP 膜剥离）。

**下位概念**：[[island-detection|孤岛]]（角度直接决定孤岛数量）、[[support-structures-resin|支撑]]（角度好 → 支撑少 → 打磨少）、[[suction-cup-effect|吸盘效应]]（角度决定截面形状）、[[anti-aliasing|像素纹/台阶纹]]（arctan 角度配合 AA 效果最佳）。

---

## 为什么角度重要

> 角度 → 决定每层截面的形状和面积 → 影响离型力（大截面 = 大吸力 = 高失败风险）→ 决定哪些区域悬空需要支撑 → 支撑数量和位置 → 打磨工作量

换个方向看：**打印是倒置的。** 每一层必须牢牢附着在上一层上。如果一个区域下方没有可附着的材料（前一层的固化树脂或支撑），它就会在液态树脂中"悬空打印" → 落到 FEP 上形成一坨固化的垃圾 → 打印失败。

角度好的标志：打开 CHITUBOX 切片预览的滑块工具，逐层检查——**每一层的形状都包含在上一层的形状之内，没有往外悬空的部分。** 此时 CHITUBOX 的模型颜色从红色（大量支撑需求）变为蓝色（安全）。

---

## 角度选择的三个核心约束

### 1. 离型力（Peeling Force）

每层曝光后平台上升，固化层必须从 FEP 膜剥离。剥离力与**当前层的截面积**成正比。

Dennys Wang 的描述：打印大截面模型时，"你能听到更大的噼啪声（snapping sound），甚至能让树脂溅出料槽"。[^1]

**操作含义**：角度越平 → 每层截面越大 → 离型力越大 → 模型被从支撑上扯下的风险越高。角度越陡 → 截面越小 → 离型力越小 → 但 Z 轴高度增加 → 打印时间变长。

### 2. 像素阶梯（Voxel Stepping）

LCD 屏幕的像素是方形的。当模型表面与像素网格不完全平行时，每一层的外轮廓由方形像素的锯齿边缘决定 → 逐层叠加形成台阶纹（[[pixel-texture|像素纹]]）。

Dennys Wang 的实测（Phrozen Sonic Mini 4K，像素 35µm，层高 0.03mm）：精确最佳角度 = `arctan(0.03 / 0.035) ≈ 40.6°`。在 arctan 角度下，每层恰好偏移一个像素宽度，台阶效应最小。[^2]

**这是一个数学约束，不是经验规则。** 但它的局限性：arctan 角度仅优化了 XY 方向的像素阶梯，没有考虑模型自身的几何形状——一个复杂曲面模型可能在 arctan 角度下反而需要大量支撑。**arctan 解决"表面光滑"，不解决"能不能打出来"。**

### 3. 支撑可及性

支撑必须放在模型上。一个好的角度应该让支撑触点落在不可见面（底部、背面、脚底）而非可见面（脸、正面、细节区域）。

Dennys Wang："人形或头雕向后倾斜，避免支撑落在鼻子和眼睛上。宁可支撑后脑勺。" [^1]

ItsMeaDMaDe："第一组支撑是最重要的支撑——它们是你倒挂房子的地基。最低点用 Heavy，稍后用 Medium，边缘曲线补 Light。" [^3]

---

## 五项原则（综合 Dennys Wang [^1]、VogMan [^4]、ItsMeaDMaDe [^3]）

### 原则 1：避免平贴平台

**现象**：模型底面完全平行于平台时，底层曝光远高于正常层（通常 30-60s vs 2s），底层和正常层的固化收缩率不同 → 打印完成后底部边缘翘曲。同时大平面平行于 FEP → 巨大离型力 → 高失败率。

**诊断**：模型拆下来后底面边缘不平整、有波浪形翘曲 → 大概率是打印时平贴了平台。

**方案**：至少绕一个轴倾斜。盒子/方形模型需要绕两个轴倾斜。[^1]

### 原则 2：最小化截面面积

**原理**：截面面积 ∝ 离型力。每层截面越小，剥离越轻松。

**实战**：将模型旋转，使每层的横截面尽可能小。长条形模型（剑、武器）应沿长度方向倾斜，而非横着打。

### 原则 3：保护可见面

**原则 2 的例外**：有时最小截面的代价是让支撑落在关键表面（脸、正面）。此时优先保护表面——原则 3 优先级高于原则 2。

人形：后仰，面部朝上。底座：垂直打印或接近垂直（ItsMeaDMaDe "75°~90°"），支撑全在底部。

### 原则 4：杯形开口朝平台

杯形、盒形模型如果开口朝上（远离平台），底部会形成封闭截面 → [[suction-cup-effect|吸盘效应]]。

**方案**：将开口倒向平台方向。Dennys Wang："倒过来，只支撑边缘，吸盘消失。" [^1]

### 原则 5：避免长直壁平行于 Z 轴

**原理**：长直壁如果在 XY 平面位置不变，每一层在 FEP 同一位置反复曝光 → FEP 局部疲劳，剥离力逐层增大。

**诊断**：打印件在中间突然断裂/出现一条横向断纹，且断裂面之前的层正常——可能是 FEP 疲劳导致的渐进式失败。

**缓解**（Dennys Wang [^1]）：如果实在无法避免直壁（如圆柱体），可以：延长正常层曝光 0.2-0.4 秒 + 增加抬升高度 2-3mm。"但这只是缓解，不是根治。"

---

## 决策框架：七步优先级

以下来自 Lychee Slicer 官方教程的体系 [^5]，按优先级从高到低排列——适用于任何切片软件，不是 Lychee 专属。

| 优先级 | 考量 | 问题 |
|---|---|---|
| 1 | **保护细节** | 正面/脸/纹理面是否朝上，远离支撑？ |
| 2 | **减少支撑** | 这个角度能否让尽量多的区域自承重而无需支撑？ |
| 3 | **减少悬空** | 是否还有大块悬空区域？旋转能否消除？ |
| 4 | **镂空排液** | 空心模型的底部是否在最低点（保证排液孔位置正确）？ |
| 5 | **减小截面** | 每层曝光面积是否尽可能小？ |
| 6 | **工程受力** | 功能性零件：打印方向是否与受力方向对齐？ |
| 7 | **打印时间** | Z 轴高度是否合理？扁平方向节省时间。 |

> **注意**：这个优先级是通用指南，不是绝对规则。同一模型可能有多个"最优"角度——寻找那些满足前 3 条、同时第 7 条可接受的方案。

---

## 常见误判

- **"30° 是万能角度"** —— ItsMeaDMaDe 明确指出："不要被一个固定角度困住。我用的是 whatever angle works best。" [^3] 每个模型的几何形状不同。
- **"arctan 角度一定最好"** —— arctan 只优化像素对齐，不解决支撑位置和离型力。复杂曲面模型需要在 arctan 附近搜索，不能死套公式。
- **"自动摆放就够了"** —— CHITUBOX 的自动摆放可以提供起点，但它不知道你的模型哪个面是"正面"、哪个细节最重要。

---

## 延伸方向

- [[island-detection|孤岛检测]]：角度确定后，下一步是逐层检查孤岛
- [[support-structures-resin|支撑]]：角度决定支撑数量和类型选择
- [[free-cutting|自由切割]]：如果最优角度仍不够 → 切分模型
- [[tolerance-and-fit|公差设计]]：多零件打印后的装配精度受角度影响

---

[^1]: Dennys Wang, "Chitubox Masterclass: How To Orient Your 3D Model" (2023). 10 年树脂打印经验，手动支撑方法论。
[^2]: Dennys Wang, "How To Get Smooth Surface With Print Angle And Antialiasing" (2021). 基于 Phrozen Sonic Mini 4K 实测，35µm 像素 / 0.03mm 层高。
[^3]: ItsMeaDMaDe, "The Perfect Angle of 3D Printing Resin | Chitubox Tutorial" (2022). 反对固定角度教条，强调逐模型判断。
[^4]: VogMan, "3D resin print supports EASY GUIDE" (2020). 基础 45° 规则及 CHITUBOX 颜色指示器使用。
[^5]: Lychee Slicer 官方教程, "How to Perfectly Orient Your 3D Model" (2024). 七步优先级框架适用于跨软件通用原则。
