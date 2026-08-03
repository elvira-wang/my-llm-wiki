---
source: "[[Any advice for these sorts of layer lines]]"
topics: [resin-printing, surface-quality, anti-aliasing, print-orientation]
form: discussion
techniques: [myth-busting, peer-debugging, diagnostic-questioning]
quality_rating: 4
created: 2026-08-03
---

# Any advice for these sorts of layer lines?

## 一句话

这条讨论把"层纹/台阶是不是靠抗锯齿解决"拆成了两个问题：XY 像素边缘可以由 AA 缓解，但更水平表面上的 Z-layer stepping 主要靠模型角度与层高/几何关系缓解。

## 内容结构

主帖先给出完整使用情境：Mars 2 Pro、0.03mm 层高、Elegoo grey ABS-like 3.0、预支撑模型、平面与曲面出现明显 stepping。评论区从"你是不是摆平了"开始追问角度，再分成两派：一派直接建议 anti-aliasing，另一派指出这是 stepping，AA 对更水平的 Z 台阶帮助有限。讨论后半段还纠正了 XY 像素分辨率与 Z 层高的维度混淆。

## 关键主张

- "AA fixes everything" 是过度简化。社区里有人明确指出 AA 主要影响垂直/边缘像素过渡，不会消除水平面上的 Z-layer stepping。
- 预支撑模型不等于最佳角度；如果有 unsupported 文件，重新按约 45° 或更适合模型的角度摆放，可能比只调 AA 更有效。
- Mars 2 Pro 的 0.05mm XY 像素与 0.03mm Z 层高是不同维度；照片上的"台阶岛"更像 Z 方向层台阶，而不只是 XY resolution。

## 表达亮点

很适合做一篇 "AA 能修什么，不能修什么" 的 Reddit/短视频内容：开头用用户的困惑切入，再用一个二维坐标解释 XY 像素纹 vs Z 层台阶。评论区的语言天然带有反迷思效果："People say AA will fix those, it won't"。

## 制作笔记

可用素材包括原帖打印照片、预支撑摆放截图、Mars 2 vs Mars 5 Ultra 像素尺寸对比。适合配一个切片软件中的倾斜角度前后对比。

## 选题信号

- Reddit 帖：`Anti-aliasing is not a magic eraser for every layer line`
- Discord 栏目：晒一张有层纹的图，让用户判断是 AA、角度、层高还是硬件分辨率。
- 短视频：前 2 秒展示"开了 AA 还是有台阶"，然后解释为什么。
