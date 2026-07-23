---
tags: [chitubox/settings, sla-printing/calibration]
source:
  - "[[CHITUBOXの印刷設定を徹底解説！自分でレジンのパラメーター調整ができるようになれば印刷も怖くない？]]"
  - "[[Chitubox 2026 v3.2.0 completo]]"
  - "[[Resin 3D Printing for Beginners Easy Step-by-Step Guide to Your First Miniatures]]"
created: 2026-07-14
domain:
  - resin-printing
  - slicing-software
confidence: consensus
knowledge_type: consensus
---

# 底层曝光

## 定义

打印最初几层时使用的特殊曝光参数——底层曝光时间远大于正常层（通常 30-60s vs 2-3s）。目的是确保最开始的几层**死死粘在构建平台上**，为整个模型的锚定提供根基。

**前置知识**：[[exposure-calibration|正常曝光校准]]（先测正常曝光 → 再调底层）。[[build-plate-leveling|平台调平]]（调平不良时，再好的底层曝光也救不了）。

**相关参数**：[[chitubox-print-settings|底层数]]——用底层曝光参数的层数；[[chitubox-print-settings|过渡层数]]——从底层曝光渐变到正常曝光。

---

## 为什么底层需要特殊曝光

正常层的固化只需"牢固附着到上一层"。底层需要"牢固附着到光滑的金属平台"。金属表面没有树脂层间的化学结合力——全靠物理吸附 + 足够的固化深度。

Dream Reich 解释得最清楚："初始层是最重要的——它是让你的打印件固定在平台上的层。如果这个曝光时间不对，你的模型会掉到料槽里，然后一定会刺穿你的 FEP 或 ACF。" [^1]

---

## 校准目标：一个平衡

不是越高越好，也不是越低越安全。目标在两端的中间：

| 太强（时间太长 / 层数太多） | 太弱（时间太短 / 层数太少） |
|---|---|
| 模型死死粘在平台上 | 中途脱落 → 掉入料槽 |
| 刮刀难拆，硬撬可能损坏模型或平台 | → 刺穿 FEP（Dream Reich:"一定会"）[^1] |
| Raft 容易碎裂 | 整板报废 |

**判断标准**：打印时牢固不脱。拆模时刮刀能正常取下——需要用力，但不死粘。

Okay Hobby Time 的调试方法："如果你的模型死死粘在平台上很难拆——降低这个数值。但别降太多，否则模型粘不住。" [^2]

---

## 影响因素

| 因素 | 影响 | 方向 |
|---|---|---|
| 树脂粘度 | 高粘度 = 流动性差 = 底层需要更长的 UV 穿透时间 | ↑ |
| 平台表面处理 | 喷砂平台附着力更强，可适当降低底层曝光 | ↓ |
| [[build-plate-leveling\|平台调平]] | 调平不良时，即使正确曝光也救不回来——接触面本身不均匀 | 无关 |
| [[temperature-control\|温度]] | 低温下树脂粘度上升 → 需要更长的底层曝光 | ↑ |

---

## 调试流程

1. 从树脂厂商推荐值或社区平均值（30-60s）起步
2. 打印一个底部有 Raft 的模型
3. 拆模时评估：轻松取下且模型无脱落 → 完美 / 死粘难拆 → 减 5-10s / 中途脱落 → 加 5-10s
4. Dream Reich 的经验：Saturn 3 Ultra + 标准树脂 → 22s 就够了（低于通用推荐区间）
   - **注意**：这是他的机器和树脂，不是你的。22s 在你机器上可能不够 [^1]

---

## 只有一侧脱落？

不是曝光问题。检查 [[build-plate-leveling|平台调平]]——脱落侧平台可能离 FEP 更远。

---

## 延伸方向

- [[chitubox-print-settings|CHITUBOX 参数]]：底层数、底层曝光时间、过渡层数
- [[build-plate-leveling|平台调平]]：物理前提——不平 = 曝光再好也失败
- [[exposure-calibration|正常曝光校准]]：先做那个，再做这个

---

[^1]: Dream Reich 3D, "Chitubox 2026 v3.2.0 completo" (2026). Saturn 3 Ultra, 底层 22s, 正常 1.9s.
[^2]: Okay Hobby Time, "Resin 3D Printing for Beginners" (2025).
