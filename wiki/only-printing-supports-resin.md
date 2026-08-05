---
tags: [sla-printing/troubleshooting, resin-slicer/troubleshooting]
source:
  - "[[Only printing supports]]"
created: 2026-08-05
domain:
  - resin-printing
  - slicing-software
  - troubleshooting
solves:
  - "[[island-detection]]"
  - "[[support-structures-resin]]"
caused_by:
  - "[[print-orientation-resin]]"
  - "[[support-structures-resin]]"
  - "[[temperature-control]]"
  - "[[manifold-geometry]]"
  - "[[release-film-wear]]"
confidence: anecdotal
knowledge_type: consensus
---

# 只打印出支撑，模型没有成型

## 定义

"只打印出支撑"指树脂打印完成后，平台上能看到 raft / support tree / sprue 等支撑结构，但模型本体缺失、掉在 FEP 上，或根本没有从某个关键层开始继续生长。它不是一个单独故障，而是一个症状：模型本体没有在早期关键层建立可靠附着。

**直觉**：支撑已经像脚手架一样长起来了，但模型的第一块"砖"没有接上脚手架。后续层再继续曝光，也只能把模型区域固化在 FEP 上、漂成碎片，或被离型力从触点上扯掉。

**前置知识**：[[island-detection|孤岛检测]]、[[support-structures-resin|树脂支撑]]、[[print-orientation-resin|打印角度]]。如果模型来自 Blender，还要先理解 [[manifold-geometry|流形几何]]。

---

## 核心因果链

> 关键最低点没有被可靠支撑 -> 模型第一批截面没有连接到平台/上一层/支撑 -> 固化区域留在 FEP 上 -> 支撑继续打印但模型不再随平台上升 -> 最终只剩支撑或一团失败残片

这个症状最常见的上游原因有五类：

| 可能原因 | 典型信号 | 验证方式 | 修正方向 |
|---|---|---|---|
| [[island-detection|最低点孤岛]] | 模型最早出现的截面不是从支撑触点开始 | 切片预览从底部逐层拖动，查看第一批模型截面下方是否为空 | 旋转模型、补最低点支撑、消除孤岛 |
| [[support-structures-resin|支撑太弱或太少]] | 支撑完整，但模型区域掉在膜上 | FEP 上有模型薄片/残块；失败位置在支撑触点附近 | 最低点用 Heavy，主体用 Medium/Light 组合 |
| [[temperature-control|温度不足或树脂太软]] | 同样支撑在软质/铸造树脂上失败 | 对照树脂厂家温度范围；测量料槽附近实际温度 | 先升温稳定，再校准曝光与支撑 |
| [[manifold-geometry|法线/非流形网格问题]] | Blender 看起来正常，切片预览缺面/反向/截面异常 | Blender Face Orientation、3D Print Toolbox、切片预览 | 翻转 normals、Make Manifold、导出前复检 |
| [[release-film-wear|离型膜释放变差]] | 同一文件曾经稳定，近期连续失败 | 检查 FEP/PFA/ACF 是否粗糙、松弛、局部释放差 | 换膜后重新调平并用小件验证 |

---

## Reddit 戒指案例

Reddit 用户在 Elegoo Mars 5 Ultra 上打印戒指，流程是 Blender 建模、在线修复、CHITUBOX 手动支撑和切片。用户为了保持戒指表面干净，只给 sprue/浇口加支撑，不想在戒指本体上留下需要打磨的支撑痕迹。四次失败后，成品只剩支撑。评论区最高价值诊断认为最低点很可能是孤岛；用户随后也注意到 sprue 底部可能确实是孤岛。[^1]

这个案例的关键不是"手动支撑一定错"，而是**表面质量优化不能抢在打印可靠性之前**。戒指、首饰、透明件、角色脸部等可见面确实要少留痕，但如果为了无痕而让第一层模型没有可靠锚点，结果会从"需要打磨"变成"完全失败"。

---

## 排查顺序

### 1. 先检查 FEP 上有没有模型残片

如果平台上只有支撑，先不要直接重打。清空或过滤树脂，检查 FEP 上是否有模型薄片、固化块或碎屑。残片说明模型区域已经曝光并固化，只是没有跟随平台上升；这会把排查重点指向 [[island-detection|孤岛]]、支撑强度、离型力或膜状态。

### 2. 看前 50 层切片预览

打开 CHITUBOX 切片预览，从底层向上逐层拖动。目标不是看最终模型好不好看，而是看模型本体第一次出现时，是否已经连接到支撑触点或上一层固化区域。

检查问题：

- 第一片模型截面是否悬空？
- 最低点是否只有 Light 支撑，甚至没有支撑？
- 支撑触点是否接在 sprue 上，但模型本体的第一层在另一个位置先出现？
- 戒指、环形件、镂空件是否同时产生 [[suction-cup-effect|吸盘效应]]？

### 3. 补强最低点，而不是盲目填满全身

不要把"更多支撑"理解成所有表面都铺满支撑。更稳的策略是：最低点和主受力点用 Heavy 或至少 Medium；非关键曲面用更轻、更密的支撑；支撑触点尽量放在内侧、背面、浇口、接口面或后续会打磨的区域。

对戒指和首饰模型尤其要分清两件事：

- **保护可见面**：避免支撑落在外侧纹理、宝石位、正面花纹上。
- **建立打印锚点**：最低点必须有足够强度承受早期离型力。

### 4. 对软质/铸造树脂提高余量

评论区指出该案例使用 Siraya Tech Cast Purple 一类铸造树脂。蜡基或铸造树脂通常更软，对温度和支撑强度更敏感；同一套支撑在普通 ABS-like resin 上成功，不代表在 castable resin 上仍然可靠。这里应按树脂厂商推荐温度和支撑强度重新建立余量，而不是复用旧支撑方案。

### 5. 检查 Blender 网格

如果 FEP 上没有明显残片，或切片预览里模型截面异常，回到 Blender 检查：

- Face Orientation 是否有红蓝反向混乱；
- normals 是否朝外；
- 是否存在 non-manifold edges、内部面、重叠面；
- 修复后重新导出 STL，并在切片预览中复检。

这一步和 [[manifold-geometry|流形几何]]、[[island-detection|孤岛检测]]是不同层级：流形/法线决定切片器能不能正确理解实体；孤岛决定正确实体在倒置打印中能不能逐层长起来。

---

## 什么时候怀疑不是支撑问题

如果同一文件、同一树脂、同一温度和同一支撑方案过去稳定成功，近期突然连续失败，要把 [[release-film-wear|离型膜老化]]、平台调平、树脂批次、温度变化、曝光漂移加入排查。一个简单方法是同时切入一个已知可靠的小模型：如果已知模型也失败，优先查机器/材料；如果已知模型成功，优先查当前戒指文件、角度和支撑。

---

## 常见误判

| 误判 | 为什么危险 |
|---|---|
| "支撑打印出来了，所以支撑没问题" | 支撑能成型只说明支撑自身能打印，不说明模型触点能承受离型力 |
| "这个支撑方案以前成功过，所以现在也该成功" | 树脂、温度、膜状态、模型方向和最早截面都可能改变 |
| "为了少打磨，先尽量不支撑模型本体" | 新模型应先保证打印成功，再逐步减少可见面支撑 |
| "在线修复过 STL，就不用看 Blender 了" | 自动修复不一定解决 normals、内部面或复杂非流形问题 |

---

## 延伸方向

- [[island-detection|孤岛检测]]：第一优先级，确认模型是否从可打印层开始生长。
- [[support-structures-resin|树脂支撑]]：最低点和受力支撑决定模型能否扛过离型。
- [[support-contact-marks-resin|树脂支撑接触痕迹]]：打印可靠性与表面清洁度之间的取舍。
- [[temperature-control|温度控制]]：软质或铸造树脂尤其依赖稳定温度。
- [[manifold-geometry|流形几何]]：Blender -> CHITUBOX 流程中的实体理解前提。

---

[^1]: Reddit, "Only printing supports??" (2026). 楼主使用 Elegoo Mars 5 Ultra、Siraya Tech Cast Purple、CHITUBOX 手动支撑；评论区诊断集中在最低点孤岛、支撑强度、温度和法线/流形问题。楼主尚未在原始材料中确认最终修复。
