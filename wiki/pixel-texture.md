---
tags: [sla-printing/surface-quality, hardware/screen]
source:
  - "[[（DLPLCD）光固化3D打印像素纹&抗锯齿详解]]"
  - "[[How To Get Smooth Surface With Print Angle And Antialiasing]]"
created: 2026-07-14
domain:
  - resin-printing
---

# 像素纹

## 定义

DLP/LCD 光固化打印中，由于像素阵列的物理结构导致模型表面出现的阶梯状纹理。本质是方形像素的直角边缘在逐层叠加后在斜面和曲面上形成的锯齿。[^1]

**直觉**：把一堆小方块叠成一座金字塔——从远处看是斜面，走近看每一级台阶都是直角方块。像素纹就是这些"台阶"在打印件上的表现。

**上位概念**：[[screen-bit-depth|屏幕位深]]（硬件能力限制 AA → 影响像素纹改善程度）。

**下位概念**：[[anti-aliasing|抗锯齿]]——改善像素纹的软件手段。[[print-orientation-resin|打印角度]]——arctan 角度配合 AA 效果最佳。

---

## 形成机制

1. LCD 屏幕上的像素在通电时透光 → 紫外光穿过像素照射树脂 → 固化形成一个有厚度的"矩形块"（体素）
2. 多个矩形块阵列排列 → 组成一层"面"
3. 面逐层叠加 → 组成模型
4. 模型外层的矩形块因其直角边角 → 逐层累积 → 在斜面/曲面上形成可见的阶梯纹理 [^1]

**本质**：像素纹是显示屏物理像素网格的"指纹"——你无法消除它，只能设法让它不那么显眼。

---

## 影响因素（按可控性排序）

| 因素 | 可控性 | 效果 |
|---|---|---|
| 屏幕物理分辨率 | 不可控（硬件） | 像素越小 → 体素越小 → 阶梯越细 |
| [[screen-bit-depth\|屏幕色深]] | 不可控（硬件） | 色深不足 → AA 效果差 → 像素纹更明显 |
| 层高 | 可控 | 层高越小 → Z 向阶梯越细 → 但打印时间成倍增长 |
| [[print-orientation-resin\|打印角度]] | 可控 | arctan 角度使阶梯与像素网格对齐 → 台阶效应最小 |
| [[anti-aliasing\|抗锯齿]] | 可控 | 灰度像素软化边缘 → 台阶效应减轻 |
| 切片格式灰度压缩 | 部分可控 | 不同格式压缩程度不同 → 影响 AA 实际效果 |

---

## 无法消除，只能管理

Zack.俞师傅的原话："像素纹无法避免，只能设法改善。" [^1] 改善的上限由硬件决定——屏幕分辨率和位深。软件手段（AA、角度）在此上限内优化。

---

## 延伸方向

- [[anti-aliasing|抗锯齿]]：改善像素纹的核心软件手段
- [[screen-bit-depth|屏幕色深]]：硬件上限——限制 AA 能好到什么程度
- [[print-orientation-resin|打印角度]]：arctan 角度是减少台阶纹的数学最优解

---

[^1]: Zack.俞师傅, "（DLP/LCD）光固化3D打印像素纹&抗锯齿详解" (v2.2.1, 2025). CHITUBOX 技术支持钟裕深监修。作者按 CC BY-NC-SA 4.0 许可。
[^2]: Dennys Wang, "How To Get Smooth Surface With Print Angle And Antialiasing" (2021). 基于 Phrozen Sonic Mini 4K 实测。
