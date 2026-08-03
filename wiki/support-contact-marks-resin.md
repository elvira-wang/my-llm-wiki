---
tags: [chitubox/workflow, sla-printing/surface-quality]
source:
  - "[[How to get rid of printing contact marks]]"
  - "[[3D resin print supports EASY GUIDE]]"
  - "[[My Support Setting - Masterclass Resin Support (MRP) 1]]"
created: 2026-08-03
domain:
  - resin-printing
  - slicing-software
  - post-processing
caused_by: [[support-structures-resin]]
confidence: consensus
knowledge_type: consensus
---

# 树脂支撑接触痕迹 (Support Contact Marks)

## 定义

支撑接触痕迹是树脂支撑从模型表面移除后留下的凸点、凹坑、撕裂或粗糙区域。它不是单纯的后处理问题，而是由 [[print-orientation-resin|打印角度]]、[[support-structures-resin|支撑参数]]、离型力、拆支撑时机和表面重要性共同决定。

---

## 为什么会留下痕迹

> 支撑触点必须足够强 -> 打印时抵抗模型重量和离型力 -> 触点与模型表面局部融合 -> 拆除时如果支撑比模型表面更抗拉，模型表面被带走 -> 形成坑；如果触点留在表面 -> 形成凸点

因此，"完全无痕"通常不是可靠目标。更现实的目标是：把痕迹放在不显眼处，让痕迹从凹坑变成可打磨凸点，并减少高细节区域的触点。

---

## 主要控制变量

| 变量 | 作用 | 风险 |
|---|---|---|
| 打印角度 | 决定哪些面需要支撑 | 横放省时间但支撑多、可见面受伤 |
| 支撑触点尺寸/深度 | 决定支撑可靠性和拆除损伤 | 太小会失败，太大会留疤 |
| 触点形状 | 球形常留下可打磨凸点，平/none 接触可能更干净 | 社区对 ball vs flat 有分歧 |
| 支撑分级 | 少量重支撑锚定 + 多个轻支撑稳定 | 全部轻支撑可能输给离型力 |
| 拆除温度 | 热水/热风会软化支撑，降低撕裂 | 热水会被树脂污染，需要按废液处理 |
| 拆除工具 | 剪钳/刀切比手撕更可控 | 粗暴手撕更容易带走表面 |

---

## 实战策略

1. 先用角度保护可见面：脸、外甲、正面纹理尽量朝上，支撑放到脚底、接口、背面、内侧。
2. 对最低点和主要承力岛使用少量 Heavy/Medium 支撑，避免整件输给离型力。
3. 其余区域用更多、更轻、更浅的支撑，不要用几个大触点硬扛全部风险。
4. 拆支撑前用热水或热风软化；如果用热水，视为可能含树脂污染的废液。
5. 凸点优先打磨；凹坑用 UV 树脂、补土或 green stuff 填补后再打磨。

---

## 常见误判

- **"支撑越少，表面越好"**：支撑太少会失败，或需要更粗触点，反而留下更大痕迹。
- **"把模型横放更快，所以更好"**：横放往往增加每层截面和支撑数量，牺牲表面质量。
- **"球形触点一定更好/更坏"**：球形触点的目标是留下可打磨凸点；如果支撑杆比球还粗、拆除太暴力，仍可能形成坑。

---

## 延伸方向

- [[support-structures-resin]]：支撑类型与最低点原则
- [[post-processing-resin]]：清洗、去支撑、固化
- [[print-orientation-resin]]：减少支撑痕迹的最上游决策

---

[^1]: Reddit, "How to get rid of printing contact marks?" (2026). 社区围绕热拆支撑、触点类型、支撑分级和角度展开经验讨论。
