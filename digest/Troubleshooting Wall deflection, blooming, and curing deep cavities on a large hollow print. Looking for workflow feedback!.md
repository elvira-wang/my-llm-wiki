---
source: "[[raw/default/Troubleshooting Wall deflection, blooming, and curing deep cavities on a large hollow print. Looking for workflow feedback!]]"
topics: [blooming, wall-deflection, hollow-printing, water-curing, fluid-dynamics, print-selection]
form: discussion
techniques: [problem-diagnosis, root-cause-analysis, tool-selection-critique]
quality_rating: 4
created: 2026-07-24
---

# Troubleshooting Wall deflection, blooming, and curing deep cavities on a large hollow print

## 一句话

一个新手用 Mars 5 Ultra + ABS-like 半透明红树脂打印大型电池收纳盒，遇到三个交织的问题——壁面变形/溢料（blooming）、深腔固化不足导致的应力开裂、以及**这个几何体本质上不应该用树脂打印**——引发了关于流体动力学、等待时间策略和"你选错了工艺"的社区反馈。

## 内容结构

OP 详细描述问题（附图和 setup）→ 分两个 issue 提问（blooming 的 root cause + 深腔固化的策略选择）→ Balerion84 给实用建议（等待时间、甘油替代水固化）→ **Lito_ 给出最尖锐的反馈**（"这个件不应该用树脂打——完全不合适"）→ OP 承认并反思（"just because you CAN doesn't mean you SHOULD"）。全长约 5 条顶层评论，集中在诊断和工艺选择。

## 关键主张

- **壁面变形 + blooming 的成因**：平台下降时，2mm 薄壁在树脂的液压下向外弯曲 → 树脂被挤入壁面与 FEP 之间的间隙 → UV 照射时将挤入的树脂固化 → 形成新月形唇边（crescent-shaped lip），只在对着平外墙那一侧出现。这是**流体动力学问题**，不是曝光问题
- **Light-Off Delay 的"够长是多长"问题**：小型件 2-3s 可能够了，但大型平壁件需要更长的等待时间让树脂从间隙中回流——没有固定值，必须测试。"Realistically, you need to find a way to not let resin get trapped in the cavities during printing if you want no blooming, or get lucky with long light off delays."
- **半透明树脂的 UV 衰减**：红色半透明树脂过滤 UV 光 → 深腔内部固化不足 → 外层完全固化 + 内层欠固化 = 应力梯度 → UV 后固化时开裂
- **深腔固化策略**：(1) 小 UV 灯泡（3-4mm）+ USB 线塞入腔内直接照射；(2) 甘油浸泡固化（比水好）；(3) 铝箔反射器反弹光线
- **"这个件根本不应该用树脂打"** — Lito_ 的核心判断：大型、功能性、平壁、深腔——这四项叠加意味着持续与流体动力学、翘曲、漏液、blooming 作斗争。OP 最终承认："just because you CAN doesn't mean you SHOULD"
- **固化前必须完全干燥**：树脂吸湿——IPA 或清洁剂吸收后必须完全蒸发（最好加热）才能进行 UV 固化

## 表达亮点

- **OP 的问题描述质量很高**——有 setup、有照片、有"我怀疑是 X 导致了 Y"的初步诊断假设。这种结构化提问方式直接得到了结构化回答
- **Lito_ 的尖锐但正确的反馈**——"This is not a resin print piece. At all."——不提供技术安慰，直接指出选错了工艺。这种诚实在 3D 打印社区中往往比委婉的技术建议更有价值
- **OP 的反思收尾**——"it got me introduced to tinkercad which was a fun learning experience"——失败但有收获，这种态度让整个讨论有了教育意义

## 制作笔记

Reddit 长文求助帖。OP 的写作风格清晰、结构化（Setup → Project → Issue 1 → Issue 2），这直接带来了高质量的社区回复。适合作为"如何有效求助"的示范案例。

## 选题信号

- "树脂打印的边界在哪里？什么时候应该换 FDM？"——这是一个被低估的选题
- "Blooming 到底是什么、怎么区分它是流体问题还是曝光问题"——许多新手把 blooming 归咎于曝光，而非液压/等待时间
- "水固化 vs 甘油固化"——有一个小型的实践者社区在做这个，但视频内容很少
- "大型平壁件的流体动力学"——跟吸盘效应、排液孔是同一个问题家族，可以做成系列
