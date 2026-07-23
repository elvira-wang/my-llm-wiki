---
tags: [sla-printing/calibration]
source:
  - "[[Resin 3D Printing for Beginners Easy Step-by-Step Guide to Your First Miniatures]]"
  - "[[3D Resin Printing ABSOLUTE BEGINNERS guide - how to 3d resin print!]]"
created: 2026-07-14
domain:
  - resin-printing
  - printer-hardware
confidence: consensus
knowledge_type: consensus
---

# 平台调平

## 定义

使构建平台的下表面与 LCD 屏幕（即 FEP 膜所在平面）完全平行的校准操作。这是光固化打印成功的第一物理前提——参数再好，平台不平全白费。

---

## 为什么必须调平

平台与 FEP 不平行时，平台一侧离膜近、另一侧远。近侧的底层被过度挤压 → 固化厚度不足；远侧间隙太大 → 树脂无法充分接触平台 → 根本不固化。打印结果：要么一部分粘住一部分脱落，要么整个模型在几层后开始倾斜→掉落。

VogMan 的表述："如果平台不平，你几乎可以保证打印失败。" [^1] Okay Hobby Time 将调平列为"最关键的一步"。[^2]

**调平不良时，再正确的 [[bottom-exposure|底层曝光]] 也救不回来**——因为模型与平台的接触面本身是不均匀的。

---

## 通用步骤

不同打印机的具体操作略有不同，但逻辑一致：

1. 松开平台固定螺丝（通常 4 颗，部分机型 2 颗）
2. 在屏幕上放置调平纸（打印机附带）
3. 将平台降至零位（Home / Z=0），平台自然压在纸上
4. 用手轻压平台顶部，让平台均匀贴合纸面
5. **按对角线顺序逐步锁紧螺丝**——先对角轻拧，再对角拧紧。不要一次拧死一颗
6. 将当前位置设为 Z=0 零点
7. 测试：抽拉调平纸，四角阻力应均匀——不能一边紧一边松

---

## 常见错误

| 错误 | 后果 | 为什么不对 |
|---|---|---|
| 用力按压平台再锁紧 | 平台倾斜——手压的力量不均匀 | 让平台自然靠自重压在纸上即可 |
| 不换调平纸反复用 | 纸被多次挤压变形，失去参考厚度 | 每次换一张新纸 |
| 先锁紧一侧再锁另一侧 | 锁第二颗时第一颗产生的应力把平台拉歪 | 对角线、逐步、均匀 |
| 更换 FEP 膜后不复调 | 新膜厚度可能不同 → 零点偏移 | 换膜必须重新调平 |

---

## 所谓"免调平"打印机

VogMan 在 2024 年时对这个说法的态度是观望："一些预算打印机声称免调平——目前来看，这个说法似乎重度依赖打印机在出厂前是否被正确调平。在得出明确结论之前，我只说一句：调平很重要，确保它做对了。" [^1]

---

## 延伸方向

- [[bottom-exposure|底层曝光]]：调平后 → 再做底层曝光校准
- [[exposure-calibration|正常曝光校准]]：调平是曝光校准的物理前提
- [[temperature-control|温度控制]]：环境条件同样影响打印成功率

---

[^1]: VogMan, "3D Resin Printing ABSOLUTE BEGINNERS guide" (2024). 面向零基础新手的完整入门。
[^2]: Okay Hobby Time, "Resin 3D Printing for Beginners" (2025).
