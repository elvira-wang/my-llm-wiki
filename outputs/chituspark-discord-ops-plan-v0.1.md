---
topics: [chituspark, discord, community-ops, pilot]
source:
  - "[[outputs/chituspark-grilling-alignment]]"
  - "[[outputs/chituspark-4-week-pilot-plan-v0.1]]"
created: 2026-08-05
status: draft-v0.1
audience: internal
---

# ChituSpark Discord 运营计划 v0.1

## 1. 核心判断

CHITUBOX Discord 当前已有 8000+ 成员，但除技术支持频道外，其他频道活跃度较低。这说明服务器里并不缺用户，缺的是一种让用户愿意低成本参与的内容机制。

第一阶段不应把 Discord 直接当成“UGC 社区”运营。UGC 门槛太高，用户不会因为品牌希望获得内容就主动贡献作品。

更现实的定位是：

> Discord 先作为 ChituSpark 的互动反馈池、素材信号池和轻量共创入口。

它不需要一开始变成热闹的大社区。第一阶段只验证三件事：

- 用户是否愿意点一下、选一下、判断一下。
- 用户是否愿意追看一次打印实验的后续结果。
- Discord 的互动是否能反哺短视频和长视频内容。

## 2. 运营目标

### 2.1 第一阶段目标

4 周内跑通一个低门槛互动机制，让 Discord 从“只在出问题时求助”扩展到“愿意参与创作过程判断”。

### 2.2 不把第一阶段定义为大社区增长

第一阶段不以服务器新增人数、全频道活跃、UGC 投稿数量为主目标。

更合适的验证指标是：

- 每周至少完成 1 个互动节点。
- 每个互动节点有真实用户选择、评论或反馈。
- 至少产出 1 条可转化为短视频的 Discord 互动素材。
- 有用户对后续结果产生追问。
- 技术支持频道以外，至少有一个轻量内容频道开始出现稳定互动。

## 3. Discord 在 ChituSpark 中的角色

Discord 不承担全部内容分发任务，它是整个内容系统中的一个节点。

| 位置 | 作用 | 说明 |
|---|---|---|
| Discord | 投票、评论、轻量共创、素材观察 | 让核心用户参与选择和判断 |
| Shorts / Reels / TikTok | 外部破圈 | 展示失败、选择、结果、反转 |
| YouTube 长视频 | 背书和教程沉淀 | 解释完整工作流 |
| Reddit | 外部信号观察和问题理解 | 观察树脂打印用户真实痛点，不硬广 |

Discord 的主要价值不是“自己热闹”，而是让 ChituSpark 的内容机制有一个可持续反馈源。

## 4. 推荐服务器结构

如果现有 Discord 不适合大改，第一阶段只建议新增或改造少量频道，避免把运营动作做得太重。

### 4.1 推荐新增一个轻量分类

分类名建议：

`ChituSpark Lab`

用途：把 ChituSpark 相关互动集中在一个轻量区域，避免污染技术支持频道，也避免散落在现有闲聊频道中。

### 4.2 推荐频道

#### `#choose-the-fix`

用途：互动打印实验主频道。

内容形式：

- 发布本周打印失败或待修复模型。
- 给出 2-3 个选项。
- 用户用表情、投票或短评论选择下一步。
- 后续公布执行结果。

用户门槛：

- 不要求用户上传作品。
- 不要求用户写长建议。
- 点一个选项也算参与。

#### `#tiny-wish-lab`

用途：愿望实现型栏目入口。

内容形式：

- 发布一个小场景，例如 Lily 的办公桌、书架角落、游戏桌一角。
- 提问“这里还可以加什么小东西？”
- 用户可以用一句话、图片参考或简单描述参与。

用户门槛：

- 不要求懂 3D 打印。
- 不要求会建模。
- 只要提出一个可被实体化的小愿望。

#### `#spark-results`

用途：结果归档频道。

内容形式：

- 公布每次实验结果。
- 放 before / after 图。
- 简短说明发生了什么。
- 链接到短视频或长视频。

价值：

- 让新来的用户快速理解栏目机制。
- 避免结果被聊天信息淹没。
- 方便后续复盘和内容整理。

### 4.3 暂不建议新增太多频道

第一阶段不要新开太多栏目频道。频道越多，空频道越多，社区越显得冷。

先用 2-3 个频道跑机制，等出现稳定互动后再扩展。

## 5. 每周运营节奏

建议先跑 4 周。

### 周节奏

| 时间    | 动作         | 目标              |
| ----- | ---------- | --------------- |
| 周一    | 发布本周互动题    | 给用户一个低门槛选择      |
| 周二-周三 | 引导评论、补充上下文 | 让讨论不冷场          |
| 周四    | 公布团队将执行的方案 | 建立“用户选择真的会影响结果” |
| 周五或周末 | 发布结果图/短视频  | 完成闭环，制造追更       |

### 每周内容量

- Discord 互动帖：1 个。
- Discord 跟进帖：1-2 个。
- Discord 结果帖：1 个。
- 可剪短视频素材：1-2 条。

## 6. 栏目 1：Choose the Fix

### 6.1 栏目定位

`Choose the Fix` 是一个打印分支实验栏目。用户不需要提供作品，只需要参与判断下一步怎么修。

一句话：

> We show a print problem. You choose what we try next. We actually print the result.

### 6.2 单期结构

#### Step 1：发布问题

内容包括：

- 一张失败图或切片截图。
- 一句具体问题。
- 2-3 个可选修复路线。
- 一个清晰投票动作。

示例：

```markdown
This tiny creature failed before it even reached the table.

What should we try first?

A. Re-orient the model
B. Add heavier supports
C. Hollow it and add drain holes

Vote below. We'll print the winning fix and post the result this week.
```

#### Step 2：中途提醒

目的不是催促，而是降低讨论门槛。

示例：

```markdown
Quick note: there may be more than one correct answer here.

If you picked A/B/C, what made you choose it?
One sentence is enough.
```

#### Step 3：公布执行方案

示例：

```markdown
The vote picked B: heavier supports.

We're setting up the reprint now. If this works, the mini survives.
If it doesn't, Round 2 begins.
```

#### Step 4：公布结果

示例：

```markdown
Result is in.

The body survived, but the staff still failed.

So this is not a full win yet. Next question:
Do we change orientation, split the part, or redesign the support contact?
```

### 6.3 主持人注意事项

- 不要一上来给标准答案。
- 不要让问题太开放。
- 不要问“大家有什么建议”，要给选项。
- 不要把用户选错包装成失败，应该表达为“我们验证了一条路线”。
- 不要强行宣传功能，只在解释过程中自然提到 CHITUBOX 工作流。

## 7. 栏目 2：Tiny Wish Lab

### 7.1 栏目定位

`Tiny Wish Lab` 是愿望实现型栏目，用于吸引不懂 3D 打印但有创作欲的人。

一句话：

> You suggest a tiny idea. We turn one into a printable object.

### 7.2 单期结构

#### Step 1：给出小场景

示例：

```markdown
Lily's desk has room for one tiny printed thing.

What should we make for it?

It can be useful, weird, cute, dramatic, or completely unnecessary.
Drop one idea below.
```

#### Step 2：筛选 3 个候选

示例：

```markdown
We picked 3 ideas from the comments:

A. A tiny mushroom lamp
B. A little dragon cable holder
C. A miniature potion bottle stand

Which one should we try to make printable first?
```

#### Step 3：执行并展示

展示从 idea 到 model 到 print 的过程。

重点不是一次成功，而是让用户看到：

- 想法如何被实体化。
- 哪些设计需要改。
- 哪些地方需要支撑或切割。
- 最终物件如何进入小场景。

### 7.3 主持人注意事项

- 不评价用户想法幼稚。
- 优先选小、低成本、低版权风险的想法。
- 避免知名 IP 仿作。
- 尽量选择能在 1 周内完成的物件。

## 8. 技术支持频道如何被使用

技术支持频道不应被强行改造成活动频道。

更合适的做法是：

### 8.1 作为信号池

观察重复出现的问题：

- 支撑失败。
- 孤岛。
- 吸盘效应。
- hollow 后破裂。
- drain hole 放置不当。
- 曝光校准困惑。
- 表面纹理或糊细节。

这些问题可以抽象成 `Choose the Fix` 的内部样板局，但不要直接搬运用户案例。

### 8.2 作为 FAQ 来源

当某个问题反复出现，可以整理为：

- 一条 Discord pinned answer。
- 一条短视频。
- 一条长视频补充说明。
- 一篇 wiki / digest 后续素材。

### 8.3 避免的问题

- 不要未经允许转发用户图片。
- 不要把用户失败案例拿去公开“点评”。
- 不要在用户求助时插入活动宣传。
- 不要把技术支持频道里的用户强行引导到新栏目。

## 9. Pilot 期间的基础指标

第一阶段建议记录非常少但有用的数据。

### 9.1 每个互动帖记录

| 指标 | 含义 |
|---|---|
| 投票/表情数 | 是否有人愿意低成本参与 |
| 有效评论数 | 是否有人愿意表达判断 |
| 追问数 | 是否有人关心结果 |
| 结果帖反应数 | 用户是否看闭环 |
| 可用素材数 | 是否能反哺短视频 |

### 9.2 4 周后判断

继续的信号：

- 每周互动节点都有人参与。
- 有用户开始解释自己的选择。
- 结果帖比普通公告更容易获得反应。
- 用户开始提出下一轮建议。
- 至少有 1-2 个互动片段可剪成外部短视频。

需要调整的信号：

- 用户只投票，不看结果。
- 用户完全不理解栏目规则。
- 选项太专业，非技术用户无法参与。
- 每期制作成本明显超过团队承受范围。
- Discord 有互动，但无法转化为短视频素材。

## 10. 4 周试运营安排

### Week 1：机制启动

目标：让用户理解“选择 -> 执行 -> 结果”的规则。

建议动作：

- 开 `#choose-the-fix`。
- 用内部样板失败件发布第一题。
- 选项控制在 3 个以内。
- 周末公布结果。

待补充：

- 第一题模型。
- 第一题失败图。
- 修复选项。

### Week 2：加入追更

目标：让用户知道上一轮选择会影响下一轮。

建议动作：

- 基于 Week 1 结果继续 Round 2。
- 如果成功，开启一个新小问题。
- 如果未完全成功，让用户选择下一步修复路线。

待补充：

- 结局语言。
- 结果图模板。

### Week 3：测试愿望型栏目

目标：验证非技术用户是否愿意参与“想法实体化”。

建议动作：

- 开一个小场景，例如办公桌或书架角落。
- 让用户提议一个小物件。
- 团队筛选 3 个候选再投票。

待补充：

- 小场景设定。
- 主角或场景命名。
- 可打印物件筛选标准。

### Week 4：闭环和复盘

目标：形成可对内复盘的完整样板。

建议动作：

- 发布 Week 3 结果。
- 做一次 “What should we try next?” 收尾帖。
- 整理 4 周互动、结果、短视频素材和用户反馈。

待补充：

- 复盘表。
- 下一阶段候选栏目。

## 11. 初始频道文案

### `#choose-the-fix` 频道说明

```markdown
Welcome to Choose the Fix.

We post a small print problem.
You vote on what we should try next.
Then we actually run the fix and share the result.

No expert answer required. A quick vote is enough.
```

### `#tiny-wish-lab` 频道说明

```markdown
Welcome to Tiny Wish Lab.

Drop a tiny idea you wish existed as a real printed object.
We will pick small, printable ideas and try to bring them to the desk.

Keep it original, small, and printable.
```

### `#spark-results` 频道说明

```markdown
Results from ChituSpark experiments live here.

Before / after prints, fixes we tried, and what we learned.
```

## 12. 我还需要了解的信息

下面这些信息会影响 v0.2 的具体执行方案。

### 12.1 服务器权限与结构

- 你是否有 Discord 服务器管理权限？
- 能否新增频道、分类、thread、poll？
- 当前服务器频道结构是什么样？
- 是否已有公告频道、作品展示频道、闲聊频道？

### 12.2 当前用户行为

- 技术支持频道每天大概有多少条消息？
- 最常见的 3 类求助问题是什么？
- 用户主要是新手、进阶用户、牙科/工业用户，还是 hobby 用户？
- 服务器里是否已有作品展示行为，只是频率低？

### 12.3 团队资源

- 谁能负责每周发帖和回复？
- 谁能负责打印复测？
- 谁能拍摄和剪辑短视频？
- 每周能承受几次真实打印实验？
- 是否有稳定可用的打印机、树脂和拍摄环境？

### 12.4 产品与功能

- 试运营期间是否可以展示新版本功能？
- AI 生模型功能是否已经能稳定生成可展示素材？
- 哪些功能可以公开露出，哪些还不能？
- 是否有需要避开的商业/合规表达？

### 12.5 品牌与账号

- ChituSpark 是否会使用独立 Discord 身份发帖？
- 发帖人是个人账号、机器人账号，还是 ChituSpark 官方身份？
- 是否已有 ChituSpark 视觉标识？
- 是否需要在 Discord 中明确说明 “from the CHITUBOX team”？

### 12.6 数据与复盘

- 上级最关心什么数据？
- 4 周后你希望拿什么结果说服团队继续？
- 是否需要做一份周报？
- 是否需要把 Discord 数据和短视频数据合并复盘？

## 13. 下一步建议

建议优先补齐三件事：

1. 当前 Discord 频道结构和权限。
2. 第一周 `Choose the Fix` 样板局。
3. 每周执行资源：谁发帖、谁打印、谁拍摄、谁剪辑。

这三件事确认后，就可以把本计划从 v0.1 推到可执行 v0.2。

