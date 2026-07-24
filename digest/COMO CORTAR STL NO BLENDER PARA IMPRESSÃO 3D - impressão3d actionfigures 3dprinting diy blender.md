---
source: "[[raw/youtube/COMO CORTAR STL NO BLENDER PARA IMPRESSÃO 3D - impressão3d actionfigures 3dprinting diy blender]]"
topics: [blender, stl-cutting, part-connection, boolean, 3d-print-prep]
form: tutorial
techniques: [step-by-step, problem-first, tool-demonstration]
quality_rating: 3
created: 2026-07-23
---

# COMO CORTAR STL NO BLENDER PARA IMPRESSÃO 3D

## 一句话

葡萄牙语教程：演示在 Blender 中用 Sculpt Mode 的 Draw Face Sets + Mask Slice 切割 STL 模型，并用 Boolean 创建连接销钉的完整分件打印工作流。

## 内容结构

两段式：**切割**（Draw Face Sets 画 mask → Fill Mask → Mask Slice to New Object）→ **连接**（创建 Cube 作为销钉 → 调整位置和尺寸 → Boolean Difference 切除槽 → Apply → 分别导出 STL）。以足球俱乐部吉祥物为示范模型。全长约 21 分钟。

## 关键主张

- Mask 上按住 Ctrl 从已涂色区域继续涂——从空白区 Ctrl+拖动会擦除 mask，这是一个容易出错的细节
- **Mask 后必须按住 Shift 沿切割线扫一遍**——让切割边缘平滑，否则切出来锯齿状
- **连接销钉必须完全嵌入零件内部**——"如果露在外面，打印时会出错"——对于 3D 打印新手来说这不是显然的
- Boolean Solver 必须用 **Exact**（中文版可能是"精确"）——3D 打印需要精确几何，不能用 Fast
- 每个连接件需要一个独立的 Boolean Modifier——如果有上下两个销钉，需要两个 Boolean 分别选两个 Cube

## 表达亮点

- **"先学怎么切，校正模型的视频下次再出"**——创作者主动划定单个视频的范围，不试图覆盖一切
- **用足球俱乐部吉祥物作为示范**——带有情感连接的模型比抽象几何体更有吸引力
- 每一步后都有视觉确认（勾选/取消视图来验证切割效果）——"看，现在有三个独立对象了"

## 制作笔记

屏幕录制 + 旁白（葡萄牙语）。节奏偏慢，适合跟随操作。创作者不回避错误——展示了 mask 颜色选错的撤销过程，增加了真实感。

## 选题信号

"怎么在 Blender 里切 STL"是跨国界的通用需求。英语市场有大量此类内容，但"切割 + 创建连接件"的组合教程相对稀缺。
