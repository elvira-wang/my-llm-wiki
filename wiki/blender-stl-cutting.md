---
tags: [3d-modeling/workflow]
source:
  - "[[youtube--COMO CORTAR STL NO BLENDER PARA IMPRESSÃO 3D]]"
created: 2026-07-23
domain:
  - resin-printing
  - fdm-printing
  - 3d-modeling
solves: [[free-cutting]]
caused_by: [[free-cutting]]
confidence: consensus
knowledge_type: consensus
---

# Blender STL 切割与连接

## 定义

在 Blender 中将 STL 模型切割为分件、并创建装配连接结构的工作流。与 [[free-cutting|CHITUBOX 自由切割]] 互补——CHITUBOX 只能做平面切割且无连接结构，Blender 可以做更复杂的切割并创建销钉、卡扣等物理连接。

---

## 为什么需要 Blender 切割

CHITUBOX 的自由切割受限于：只能平面切割、无连接结构设计、不支持曲面切割面。当模型超出平台、需要隐藏接缝、或需要可拆卸装配时，Blender 提供了更完整的解决方案。

Alien Explorer 的典型场景：AI 生成的完整角色需要拆分成头、手臂、身体、腿分别打印——"每一块都需要连接件来装配。" [^1]

---

## 完整工作流

### 步骤 1：导入 STL

拖拽 STL 文件到 Blender 视口 → Import STL。或 `File → Import → STL (.stl)`。

导入后模型默认在原点。如果模型中心偏离，`Object → Set Origin → Geometry to Origin`。

### 步骤 2：在 Sculpt Mode 用 Mask 画切割线

切换到 Sculpt Mode。选择 **Draw Face Sets** 笔刷——这个笔刷在模型表面涂色，用于标记不同区域。

**关键操作**：
- 涂色：直接在表面拖动笔刷，涂上一种颜色
- **继续涂同色**：松手后想继续涂同一区域 → **按住 `Ctrl` 从已涂色区域开始拖动**（从空白区开始 `Ctrl+拖动` = 擦除 mask）
- 调整笔刷大小：按 `F`，移动鼠标
- **画完后按住 `Shift` 沿切割线轮廓轻扫**——这会让切割边缘更平滑 [^1]

**注意事项**：
- 每一块颜色 = 一个独立的 mask 区域。如果无意中换了颜色，Ctrl+Z 撤销
- 切割线不能有缺口——如果 mask 边缘有缝隙，切割后的 mesh 边缘会不完整
- 要切割的地方必须被不同颜色的 mask 完全包围

### 步骤 3：执行切割

1. 按 `H` 隐藏未 mask 部分，确认 mask 覆盖正确
2. `Mask → Fill Mask`（填充 mask 内部，如有需要）
3. 按 `Shift+H` 恢复显示
4. `Mask → Mask Slice to New Object`

这会创建两个独立对象：原模型（减去 mask 区域）和切下来的部分。

### 步骤 4：创建连接结构

回到 Object Mode，选择主体模型。

**创建连接销钉**：
1. `Shift+A → Mesh → Cube`
2. 缩放到合适尺寸（连接件必须足够粗——"太细会在打印时断裂" [^1]）
3. 定位到切面的中心位置——**连接件必须嵌入两个零件的内部**，不能只贴在表面。"如果连接件露在外面，打印时会出错。" [^1]
4. 可选：`Tab → Edit Mode → 选择顶面 → 缩放` 让销钉顶部略微变细——形成楔形导向，便于装配

**复制连接件**：`Ctrl+C → Ctrl+V` → 旋转/移动到第二个零件的对应位置。

### 步骤 5：用 Boolean 在零件上切出连接槽

选择需要被切割的零件 → `Modifier Properties → Add Modifier → Boolean`。

| 参数 | 设置 |
|---|---|
| Operation | **Difference**（切除） |
| Object | 选择连接销钉（用吸管工具点选） |
| Solver | **Exact**（精确模式——3D 打印需要精确几何） |

点击 Apply 使切割永久生效。

**每个连接件需要单独的 Boolean Modifier**——如果有上下两个销钉，需要两个 Boolean，分别选择两个 Cube 对象。Alien Explorer 的做法是先加一个 Boolean 选择上方的销钉，再加第二个 Boolean 选择下方的销钉，最后 Apply。[^1]

### 步骤 6：导出分件

- 每个分件单独导出：隐藏其他对象 → `File → Export → STL`
- 勾选 Selection Only → 命名导出
- 对所有分件重复

---

## 与 CHITUBOX 自由切割的对比

| | [[free-cutting\|CHITUBOX 自由切割]] | Blender STL 切割 |
|---|---|---|
| 切割面类型 | 只能平面 | 任意形状（沿 mask 轮廓） |
| 连接结构 | 无（需要第三方建模） | 可创建销钉、卡扣等 |
| 学习成本 | 低（切片软件内操作） | 中（需要 Blender 基础知识） |
| 适用场景 | 快速切分、模型超出平台 | 需要精确装配、复杂分件 |
| 工作流位置 | 在切片软件内完成 | 在建模软件中完成 → 导出 STL → 导入切片软件 |

**选择标准**：如果只需要简单切分以便放入平台 → CHITUBOX 自由切割。如果需要可拆卸装配、隐藏接缝、多零件配合 → Blender。

---

## 延伸方向

- [[free-cutting|自由切割]]：CHITUBOX 内置的平面切割方案——更简单但功能有限
- [[part-joining-methods|零件连接方法]]：销钉、卡扣、T 槽等专业连接结构设计
- [[tolerance-and-fit|公差与配合]]：连接件尺寸需要考虑材料收缩和打印公差
- [[manifold-geometry|流形几何]]：Boolean 切割后务必检查 manifold

---

[^1]: Alien Explorer, "COMO CORTAR STL NO BLENDER PARA IMPRESSÃO 3D" (2025). 葡萄牙语教程，演示完整的 Mask → Slice → Boolean → 导出流程。使用 Blender 4.3。
