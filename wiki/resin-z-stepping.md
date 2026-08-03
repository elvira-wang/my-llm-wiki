---
tags: [sla-printing/surface-quality, chitubox/settings]
source:
  - "[[Any advice for these sorts of layer lines]]"
  - "[[How To Get Smooth Surface With Print Angle And Antialiasing]]"
created: 2026-08-03
domain:
  - resin-printing
  - slicing-software
  - surface-quality
caused_by: [[print-orientation-resin]]
confidence: consensus
knowledge_type: consensus
---

# 树脂 Z 层台阶 (Resin Z-Stepping)

## 定义

Z 层台阶是模型表面因为逐层堆叠而形成的可见阶梯，常出现在接近水平的斜面、曲面峰值、披风、平板、枪身等区域。它和 [[pixel-texture]] 有关系，但不是同一个问题。

**区别**：

| 问题 | 主要方向 | 典型解决 |
|---|---|---|
| [[pixel-texture]] | XY 屏幕像素边缘 | [[anti-aliasing]]、灰度/模糊、屏幕分辨率 |
| Z 层台阶 | 层高 + 表面斜率 | [[print-orientation-resin]]、层高、后处理 |

---

## 为什么 AA 不能擦掉所有层纹

[[anti-aliasing]] 的核心作用是让切片边缘像素从全亮/全暗变成灰度过渡，改善 XY 边界的硬台阶。它对垂直或接近垂直的边缘更有效。

但当问题来自更水平表面的 Z 向层级时，AA 无法改变每层实际堆叠的高度。Reddit 讨论中有用户把这种现象称为 stepping，并指出 AA 不会修复更水平表面的 Z 台阶；更有效的方法是重新摆放模型角度。[^1]

---

## 因果链

> 表面接近水平 -> 相邻层外轮廓变化较大 -> 每层边界在可见面形成一圈台阶 -> 层高越大或表面越平缓，台阶越明显 -> AA 只能软化边缘，不能消除层间高度差

这解释了为什么用户已经用 0.03mm 层高，仍会在某些平面/曲面看到明显 stepping：问题不只是层高数值，还取决于模型局部表面的倾斜角。

---

## 处理策略

| 策略 | 解决什么 | 代价 |
|---|---|---|
| 改变角度 | 让台阶分散到更不显眼区域，减少水平表面阶梯 | 可能增加支撑或打印时间 |
| 降低层高 | 减小每级台阶高度 | 打印时间增加 |
| 使用 AA / blur | 改善 XY 边缘与像素纹 | 细节可能变糊，不能根治 Z 台阶 |
| 打磨 / 喷底漆 / 后处理 | 成品阶段隐藏纹理 | 增加手工成本，细节区风险高 |

---

## 常见误判

- **"Mars 2 Pro 的 0.05mm 像素导致所有这些线"**：XY 像素会影响边缘纹理，但照片中像"阶梯岛"一样的水平层纹更可能是 Z 层台阶与摆放角度共同造成。
- **"预支撑模型角度一定正确"**：预支撑只说明作者给了一个能打印的方案，不保证对你的打印机、层高、目标表面质量最优。
- **"开 AA 就行"**：AA 是工具，不是万能橡皮擦。

---

## 延伸方向

- [[anti-aliasing]]：改善 XY 边界
- [[print-orientation-resin]]：控制 Z 台阶可见性、支撑位置与离型力
- [[pixel-texture]]：屏幕像素造成的表面纹理

---

[^1]: Reddit, "Any advice for these sorts of layer lines?" (2026). 社区围绕 AA、角度、XY 分辨率与 Z 层台阶展开讨论。
