---
source: "[[Only printing supports]]"
topics: [resin-printing, troubleshooting, supports, islands, jewelry-printing]
form: discussion
techniques: [peer-debugging, diagnostic-checklist, tradeoff-framing]
quality_rating: 4
created: 2026-08-05
---

# Only printing supports??

## 一句话

这是一个典型的"支撑打出来了、模型没跟上"诊断案例：用户为了保护戒指表面，只给 sprue/浇口加手动支撑，评论区把根因集中到最低点孤岛、支撑强度不足、软质铸造树脂温度，以及 Blender 网格法线/流形问题。

## 内容结构

主帖给出完整但新手化的流程：Blender 建模 -> formware.co 修复 -> CHITUBOX 手动加支撑 -> Elegoo Mars 5 Ultra 网络发送 -> 四次都只剩支撑。最高价值评论先指出"最低点是孤岛"，楼主也意识到 sprue 底部可能确实没有被正确接住。第二组评论追问自动支撑 vs 手动支撑，暴露出核心取舍：用户不想支撑戒指本体，因为怕打磨破坏表面。后续评论补充 Siraya Tech Cast Purple 对温度和中/重支撑更敏感，以及可能存在 inverted normals、non-manifold 或更深层网格错误。最后有人建议放入一个已知可打印模型做对照，以区分文件问题和机器/材料问题。

## 关键主张

- "只打印支撑"通常不是网络发送或切片按钮的问题，而是模型本体没有在第一批关键层建立可靠附着：最低点孤岛、支撑太弱、离型力过大或模型几何被切片器误解。
- 为了避免支撑痕迹而只支撑浇口/不支撑模型本体，是首饰和精细模型里的高风险策略；成功打印优先于无痕支撑，尤其在新模型或新树脂上。
- Castable / wax-based resin 更软、更吃温度和支撑强度；同样的支撑方案在普通树脂上成功，不代表在铸造树脂上仍有余量。

## 表达亮点

这条适合做"不要把支撑痕迹优化放在打印成功之前"的内容。它不是单一答案，而是一个排查树：先看 FEP 上有没有模型残片，再回到切片预览检查第一层模型区域，然后补最低点和中/重支撑，最后检查法线/流形并用已知模型做 A/B 对照。

## 制作笔记

可做成 CHITUBOX/Discord 的失败排查模板：上传失败照片、切片预览最低 50 层、支撑截图、树脂型号、温度、是否 castable resin、Blender face orientation 截图。素材中 Siraya Tech 官方温度与支撑建议来自评论转述，写内容时应标为二手引用并回查官方页面。

## 选题信号

- Reddit：`Only supports printed? Check the model's first printable layer, not just the support count.`
- Discord：发起"只剩支撑"诊断帖模板，要求先贴 FEP 残片和前 50 层预览。
- 短视频：错误做法"只支撑浇口保护表面" -> 切片预览最低点孤岛 -> 补中/重支撑后的对比。
