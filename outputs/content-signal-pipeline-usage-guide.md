---
title: "Content Signal Pipeline 使用说明"
created: 2026-08-03
applies_to: content-signal-pipeline
status: guide
---

# Content Signal Pipeline 使用说明

## 一句话

`content-signal-pipeline` 是从素材到发布的内容生产工作流。

它的核心原则是：

**先从素材里发现真正值得讲的选题，再排内容日历，最后生成当天可发布内容。**

不要让内容日历反过来锁死选题。日历只是排班，选题判断来自素材、digest、wiki、web research 和业务目标。

## 四层产物

| 层级 | Mode | 回答的问题 | 输出目录 | 是否依赖日历 |
|---|---|---|---|---|
| 1 | `signal-board` | 本周/这个主题里有哪些值得关注的信号？ | `outputs/content-signals/` | 不依赖 |
| 2 | `topic-package` | 哪些信号能发展成选题？推荐哪个先写？ | `outputs/topic-packages/` | 不依赖 |
| 3 | `calendar` | 这些选题什么时候、用什么栏目发？ | `outputs/content-calendars/` | 依赖信号板或选题包 |
| 4 | `daily-publishing-package` | 今天这条最终发什么标题、正文、首评、素材？ | `outputs/content-packages/` | 依赖日历 slot |

完整链路：

```text
raw / digest / wiki / web / user idea
  -> signal-board
  -> topic-package
  -> calendar
  -> daily-publishing-package
  -> published post
  -> metrics / learnings
```

## 关键规则

### 1. `topic-package` 可以单独生成

如果你的任务是：

- 从本周 Reddit 热帖里找 3 个选题
- 从一批素材里判断哪个值得做
- 推荐一个选题并写草稿方向
- 为 Discord / Reddit / short video 找栏目灵感

这都应该生成 `topic-package`，不需要先有内容日历。

### 2. `calendar` 不产生最终文案

内容日历只保存：

- 日期
- 时间
- 栏目
- `working_title`
- `signal_id`
- `topic_package_id`
- `daily_package_file`
- 状态

`working_title` 是暂定方向，不是最终标题。最终标题和正文在 `daily-publishing-package` 里确定。

### 3. 问“今天发什么”时必须读 daily package

当你问：

```text
今天在 reddit 发布的内容和时间
```

正确流程是：

1. 读取最新 content calendar。
2. 找到今天的 calendar slot。
3. 读取该 slot 的 `Daily Package File`。
4. 如果 daily package 存在，直接从里面提取发布时间、标题、正文、首评。
5. 如果 daily package 不存在，说明“今天已有排期，但 final package 还没生成”，然后再生成。

不要只看日历就即兴写正文。

## ID 规范

| ID | 含义 | 示例 |
|---|---|---|
| `signal_id` | 一个可复用内容信号 | `sig-reddit-fep-release-film` |
| `topic_package_id` | 一个选题包 | `topic-reddit-chitubox-weekly-2026-08-03` |
| `calendar_slot_id` | 一个发布排期 slot | `reddit-2026-08-03-case-fep` |
| `daily_package_file` | 某天最终发布包 | `outputs/content-packages/reddit-2026-08-03-case-fep.md` |

## 常用 Prompt 样例

### A. 生成信号板

用于回答“这周有什么值得讲”。

```text
使用 content-signal-pipeline，以 signal-board 模式，基于本周 raw/reddit、digest 和 wiki，为 CHITUBOX Reddit 官方 subreddit 生成本周内容信号板。

请重点识别：
1. 用户真实痛点
2. confirmed fix
3. 社区争议
4. 适合官方账号介入的角度
5. 不适合官方账号下结论的风险点
```

### B. 生成周选题包

用于回答“给我 3 个选题，并推荐 1 个”。

```text
使用 content-signal-pipeline，以 topic-package 模式，基于最新 signal board 和本周 raw/reddit 里与 CHITUBOX 相关的热门讨论，生成 3 个适合 Reddit 发布的帖子选题，并推荐 1 个写成草稿方向。

要求：
- 不依赖内容日历
- 每个选题说明用户痛点、信源、wiki 支撑、风险
- 推荐 1 个最适合优先写
- 给出 Reddit、Discord、短视频的复用方向
```

### C. 从某个素材直接生成选题包

用于用户自己提取了一个素材或想法。

```text
使用 content-signal-pipeline，以 topic-package 模式，基于 raw/reddit/Hollow issues.md 和相关 wiki，判断这个素材是否值得做成 CHITUBOX 官方 Reddit 内容。

请输出：
1. 是否值得做
2. 最适合的 Reddit 角度
3. 是否更适合 Discord 或短视频
4. 可用素材
5. 需要避免的绝对化说法
```

### D. 生成 2 周 trial 内容日历

用于把已经筛过的选题排成栏目。

```text
使用 content-signal-pipeline，以 calendar 模式，基于最新 signal board 和 topic package，为 CHITUBOX 官方 subreddit 生成 2 周 trial 内容日历。

要求：
- 周一到周五每天 1 条
- 每周 1 条 Community Case File
- 日历只写 working title，不写最终标题
- 每个 slot 必须包含 signal_id、topic_package_id、calendar_slot_id、daily_package_file、status
- 标注哪些 slot 还需要生成 daily publishing package
```

### E. 生成某一天的最终发布包

用于从 calendar slot 生成当天可发布内容。

```text
使用 content-signal-pipeline，以 daily-publishing-package 模式，生成 calendar slot `reddit-2026-08-04-myth-aa-z-stepping` 的 Reddit 发布包。

请读取：
1. 对应 content calendar
2. 对应 topic package
3. 对应 signal board
4. 相关 digest / wiki / raw

输出：
- 最终标题
- 主帖正文，120-220 words
- 可选首评
- 信源和准确性提醒
- 发布建议
```

### F. 查询今天发什么

用于每天发布前。

```text
今天在 Reddit 发布的内容和时间。

请严格按 content-signal-pipeline 的 daily-publishing-package 查询规则执行：
1. 先查今天的 calendar slot
2. 再读取该 slot 的 daily_package_file
3. 如果文件存在，直接提取发布时间、标题、正文、首评
4. 如果文件不存在，告诉我缺少 daily package，不要即兴重写
```

### G. 发布后回填数据

用于复盘。

```text
使用 content-signal-pipeline，更新 reddit trial calendar 的 retrospective slots。

已发布 slot：reddit-2026-08-03-case-fep
Post URL: [粘贴链接]
24h comments: [数字]
Useful replies: [简述]
Negative signals: [如有]
Learning: [这条内容告诉我们什么]
```

### H. 两周后复盘并生成下一轮日历

```text
使用 content-signal-pipeline，基于 2 周 trial calendar 的 retrospective slots、Reddit 评论反馈、最新 raw/reddit 和 digest，复盘哪些栏目应该保留、调整或停止。

然后生成下一轮 2 周内容日历。
要求：
- 先更新 signal board
- 再生成 topic package
- 最后生成 calendar
- 不要直接从旧日历复制排期
```

## Reddit 日更内容长度建议

| 类型 | 主帖正文长度 | 使用频率 |
|---|---:|---|
| 轻量讨论帖 | 50-120 words | 可穿插 |
| 日更标准帖 | 120-220 words | 默认 |
| mini-guide | 250-450 words | 每周 1-2 条 |
| 深度教程 | 500-900 words | 偶尔，最好配图 |

日更主帖不要塞太多证据。证据、链接、免责声明和长 checklist 放首评。

## Reddit 官方 subreddit 的栏目建议

| 星期 | 栏目 | 作用 |
|---|---|---|
| Monday | Community Case File | 转帖/案例归档 + 官方首评解析 |
| Tuesday | Slicer Myth | 破除一个切片或打印误区 |
| Wednesday | Tiny Checklist | 一个可执行检查表 |
| Thursday | Ask the Community | 收集用户参数、经验、判断阈值 |
| Friday | Fix in 5 Steps | 周末打印前的小教程 |

## 常见错误

### 错误 1：直接从日历写正文

不对。日历只有 working title 和栏目，不是最终内容源。

正确做法：

```text
calendar slot -> daily_package_file -> publishable copy
```

### 错误 2：让内容日历决定选题

不对。日历只能安排已经被判断过的选题方向。

正确做法：

```text
signal-board -> topic-package -> calendar
```

### 错误 3：把周选题包当成当天发布包

不对。周选题包是上游判断文件。

正确做法：

```text
topic-package: 选题判断
daily-publishing-package: 当天最终发布文案
```

### 错误 4：缺 daily package 时即兴重写

不对。应该明确告诉用户缺 final package，并询问或直接生成。

## 当前示例文件

| 类型 | 文件 |
|---|---|
| Signal board | `outputs/content-signals/reddit-chitubox-signal-board-2026-08-03.md` |
| Topic package | `outputs/topic-packages/reddit-chitubox-weekly-topics-2026-08-03.md` |
| Trial calendar | `outputs/content-calendars/reddit-chitubox-2-week-trial-calendar-2026-08-03.md` |
| Daily publishing package | `outputs/content-packages/reddit-2026-08-03-case-fep.md` |
