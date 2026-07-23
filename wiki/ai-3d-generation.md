---
tags: [sla-printing/workflow, 3d-modeling/workflow]
source:
  - "[[youtube--AI Image to 3D Print - Complete Workflow (Hunyuan 3D + Blender)]]"
  - "[[youtube--From AI Image to Printed 3D Figure (Best & Fastest Tutorial)]]"
created: 2026-07-23
domain:
  - resin-printing
  - 3d-modeling
  - ai-tools
confidence: consensus
knowledge_type: consensus
---

# AI 图像到 3D 打印

## 定义

使用 AI 3D 生成器将 2D 图像转换为可直接 3D 打印的实体模型的完整流程。核心理念：**AI 生成的是起点，不是终点——原始 AI 输出永远不能直接切片打印**，必须经过 Blender 清洗。

---

## 为什么必须清洗 AI 生成的网格

AI 生成器（Hunyuan 3D、Hitem3D、TripoAI 等）的目标是"看起来像"，不是"能打印"。它们的输出存在系统性缺陷：

| 缺陷 | 原因 | 后果 |
|---|---|---|
| 顶点未合并 | 生成算法的面片拼接不精确 | 相邻面看似连着，实际有微米级间隙 → 非流形 |
| 内部残留几何 | 生成过程中产生的碎片 | 切片时内部出现不该有的实体 |
| 细薄悬空结构 | 算法不理解物理可行性 | 打印时断裂或无法成型 |
| 空洞和间隙 | 生成几何不完整（如头发和脖子之间） | 切片产生异常截面，打印失败 |
| 面数过高 | 1.5M+ 面的生成默认值 | 切片软件处理极慢，且对实际精度无益 |

PixelArtistry 的实测："每次从 AI 导入模型，第一件事就是 merge vertices by distance——你会看到它移除了大量顶点。" [^1] Stefan 3D AI 补充："如果你直接打印 AI 原始输出，你会发现空腔、孔洞和薄到无法打印的细节。" [^2]

---

## 完整工作流

### 阶段 1：生成 2D 参考图

使用 Midjourney、Nano Banana（Gemini）、Stable Diffusion 等生成角色的正面 T-pose 图。

**提示词模板**（Midjourney）：`Full body character design, [角色描述], T-pose, neutral lighting, simple background, 3d render style --style raw --ar 1:1`

**为什么必须 T-pose**：T-pose（双臂平伸、腿并拢）是标准绑定姿态——后续要在 Blender 中 rig 和 pose。如果 AI 输出的角色已经摆了姿势，手臂交叉处、手贴身体处会产生无法清理的交叠几何。

**Nano Banana 修正**：如果 2D 图不是标准 T-pose，用 Nano Banana（Gemini Pro）指令 `take this character and put him in a T-pose for rigging, make sure hand palms are facing down` 修正。[^1]

### 阶段 2：AI 生成 3D 网格

以 Hunyuan 3D 3.0 为例：
- 上传 T-pose 参考图
- 设置：Version 3.0, Face Count 1.5M, Geometry + Texture
- 下载 GLB 格式 → 导入 Blender

其他工具：Hitem3D（Stefan 推荐，几何精度更好 [^2]）、TripoAI、MeshyAI、3DAIStudio。各工具的几何质量和缺陷类型不同——Stefan 维护了一个独立排行榜。[^2]

### 阶段 3：Blender 清洗（不可跳过）

**3.1 合并顶点**
`Edit Mode → A（全选）→ Right Click → Merge Vertices → By Distance`。移除生成产生的微间隙。Stefan 强调：如果后续要做 remesh 或 rigging，merge distance 要设得比默认 0.001 大——"0.001 不够让 rigging 成功，必须提高。" [^2]

**3.2 清理材质和法线**
- Material 标签页：移除 AI 自带的材质（对打印无用）
- Geometry Data：`Clear Custom Split Normals`——AI 生成的法线数据通常有误

**3.3 Remesh**
`Modifiers → Remesh → Voxel Size ~0.005–0.01`。目的：
- 统一拓扑结构（AI 输出的三角面分布不均匀）
- 消除非流形边
- 为雕刻提供均匀的基础网格

"Voxel size 不要设太小——Blender 会崩溃。0.005 已经能保留绝大多数细节，同时把面数控制在可管理的范围。" [^1]

**3.4 雕刻修复**
- **平滑笔刷**（`Shift + 左键`）：消除 AI 生成的表面噪点和伪影——"我估计 50% 的清洗时间都在做平滑" [^2]
- **弹性抓取**（Elastic Grab）：调整形状——"就像用手捏粘土一样移动几何体" [^2]
- **膨胀笔刷**（Inflate）：填充小间隙和孔洞
- **Blob/Clay Strips**：添加缺失的体积（如眼球、衣褶）

### 阶段 4：封闭空洞和间隙

AI 生成的角色常见问题：头发和脖子之间有空隙、衣服下摆下方开放、薄花/薄叶中间有洞。Stefan 的方法：

**方法 A — 用几何体填补大空洞**：`Shift+A → Mesh → Circle → F（填面）→ Subdivision Surface → 缩放定位 → Sculpt Mode 弹性抓取对齐轮廓 → Join + Remesh`。[^2]

**方法 B — Mask Slice 复制轮廓**：复制模型 → Mask 选取需要填充轮廓的区域 → Mask Slice to New Object → 弹性抓取移动 → 填充间隙 → Join + Remesh。[^2]

**关键原则**："用膨胀或弹性抓取填充间隙后，必须再 remesh 一次——否则两个 mesh 只是穿插在一起，不是真正融合。不 remesh 就去做平滑，结果会很差。" [^2]

### 阶段 5：Rig 和 Pose（可选）

用于给 T-pose 模型摆姿势：
1. `Shift+A → Armature → Human (Meta-Rig)` → 缩放对齐模型
2. Edit Mode 调整骨骼位置，启用 X-Axis Mirror
3. 选择 mesh → 选择 armature → `Ctrl+P → With Automatic Weights`
4. **常见失败**："Bone heat weighting failed to find solution"——回到 Edit Mode → `A → Merge Vertices → By Distance`（增大 merge 距离）→ 重新绑定
5. Pose Mode 摆姿势 → 完成后在 Modifier 中 Apply Armature

### 阶段 6：准备导出

1. 确认尺寸：Scene Properties → Units → Metric / Millimeters。Hunyuan 3D 默认生成约 20cm 高的模型
2. 如果面数仍过高 → `Modifier → Decimate` 适度降低（打印不需要百万面）
3. `3D Print Toolbox → Check All` → 确保 Non Manifold Edges = 0
4. `File → Export → STL`，勾选 Selection Only

---

## 注意事项

- **小模型（<7cm）可以实心打印**，不需要镂空——省去打排液孔的步骤 [^2]
- **AI 生成后修复比从零建模快**，但并非零技能——需要理解 Blender 的 sculpt、remesh 和 Boolean 基础
- **不同 AI 工具的缺陷模式不同**——Hunyuan 3D 的表面质量好但常有内部碎片，Hitem3D 的几何更精确但细节可能不如
- **二次创作时考虑版权**——AI 生成的角色形象可能涉及原作 IP

---

## 延伸方向

- [[manifold-geometry|流形几何]]：AI 网格最常见的缺陷——非流形边
- [[hollowing|镂空]]：大模型打印前镂空节省树脂
- [[support-structures-resin|树脂支撑]]：AI 角色通常需要大量支撑——摆放角度至关重要
- [[print-orientation-resin|打印角度]]：角色脸朝上、背朝下——保护可见面

---

[^1]: PixelArtistry, "AI Image to 3D Print - Complete Workflow (Hunyuan 3D + Blender)" (2026). 完整的 Midjourney → Hunyuan 3D → Blender → 打印流程。包含 rigging 和 pose 的详细步骤。
[^2]: Stefan 3D AI, "From AI Image to Printed 3D Figure (Best & Fastest Tutorial)" (2026). 客户付费项目实战案例——$150 定制人偶，成本约 $30。重点覆盖几何修复和空洞填充技巧。
