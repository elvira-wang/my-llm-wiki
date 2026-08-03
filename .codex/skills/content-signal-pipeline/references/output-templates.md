# Output Templates

## Signal Board

```markdown
---
title: "[channel/topic] signal board"
created: YYYY-MM-DD
mode: signal-board
platform:
business_goal:
source_window:
---

# Signal Board: [channel/topic/date]

## Recommendation

| Rank | Signal ID | Topic | Best Next Artifact | Why |
|---|---|---|---|---|
| 1 | sig-[channel]-[topic] |  | calendar / content-package / hold |  |

## Candidate Signals

| Signal ID | Topic | User Pain | Trigger Scene | Evidence | Wiki Support | Platform Fit | Risk | Priority |
|---|---|---|---|---|---|---|---|---|
| sig-[channel]-[topic] |  |  |  | raw/digest/wiki/web paths | wiki links | Reddit / Discord / short video | low / medium / high | high / medium / low |

## Scoring

| Signal ID | Audience Urgency | Knowledge Leverage | Community Fit | Product Fit | Evidence Quality | Asset Availability | Total |
|---|---:|---:|---:|---:|---:|---:|---:|
|  |  |  |  |  |  |  |  |

## Calendar Guidance

- Best column:
- Best weekday:
- Recommended format:
- First topic package or daily package to generate:

## Hold / Reject

| Signal | Reason |
|---|---|
|  |  |
```

## Content Calendar

```markdown
---
title: "[channel] content calendar"
created: YYYY-MM-DD
mode: calendar
status: trial / active / archived
signal_board:
period:
  start: YYYY-MM-DD
  end: YYYY-MM-DD
---

# [Channel] Content Calendar

## Calendar Logic

- Source basis:
- Business goal:
- Cadence:
- Posting time test:

## Slots

| Date | Time | Calendar Slot ID | Signal ID | Topic Package ID | Column | Working Title | Format | Source Base | Topic Package | Daily Package File | Status | CTA |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| YYYY-MM-DD |  | [channel]-YYYY-MM-DD-[column]-[topic] | sig-[channel]-[topic] | topic-[channel]-[topic] |  |  |  |  | outputs/topic-packages/[file].md | outputs/content-packages/[file].md | planned / package-needed / drafted / published / skipped |  |

## Retrospective Fields

Track after publishing:

| Calendar Slot ID | Post URL | 24h Comments | 72h Comments | Useful Replies | Negative Signals | Learning |
|---|---|---:|---:|---:|---|---|
```

## Topic Package

```markdown
---
title: "[channel/topic] topic package"
created: YYYY-MM-DD
mode: topic-package
topic_package_id: topic-[channel]-[topic/date]
platform:
channel:
calendar_dependency: none
source_window:
signal_board:
recommended_calendar_slots:
---

# Topic Package: [topic/channel/date]

## Recommendation

| Rank | Topic | Recommended Use | Why | Confidence |
|---|---|---|---|---|
| 1 |  | draft / calendar / hold |  |  |

## Signal Table

| Topic | Signal ID | User Pain | Evidence | Channel Fit | Product Fit | Risk |
|---|---|---|---|---|---|---|
|  | sig-[channel]-[topic] |  | raw/digest/wiki/web paths |  |  |  |

## Evidence And Materials

- Wiki:
- Digest:
- Raw:
- Web:
- Visual assets:

## Recommended Draft Direction

- Title direction:
- Audience:
- Thesis:
- Content shape:
- First comment / source strategy:

## Calendar Fit

- Best column:
- Best weekday:
- Suggested working title:
- Suggested CTA:

## Accuracy Notes

- What is confirmed:
- What is debated:
- What should not be claimed:
```

## Daily Publishing Package

```markdown
---
title: "[title]"
created: YYYY-MM-DD
mode: daily-publishing-package
platform:
column:
signal_id:
topic_package_id:
calendar_slot_id:
calendar_file:
status: draft
post_url:
---

# Daily Publishing Package: [title]

## Brief

- Channel:
- Audience:
- Goal:
- Signal ID:
- Topic package:
- Calendar slot:
- Thesis:
- Recommended format:

## Why This Works

- Audience urgency:
- Community tension:
- Knowledge leverage:
- Product fit:

## Evidence

| Claim | Confidence | Source |
|---|---|---|
|  | established / consensus / anecdotal / debate / speculative |  |

## Materials

- Wiki:
- Digest:
- Raw:
- Web:
- Visual assets:

## Outline

1. Hook / opening scene
2. Misbelief
3. Mechanism
4. Practical workflow
5. Invitation / CTA

## Draft

[Platform-specific draft]

## Reuse

- Reddit:
- Discord:
- Short video:

## Accuracy Notes

- What is confirmed:
- What is debated:
- What should not be claimed:
```

## Reddit Draft

```markdown
# [Recommended title]

## Daily Post

Target: 120-220 words for Monday-Friday daily posting. Use a peer-to-peer field note, short diagnosis, or discussion prompt. Mention the product only when it naturally belongs in the workflow.

[Opening: community problem or field observation]

[One compact evidence-backed insight]

[Short practical takeaway]

[Question for the community]

## Optional First Comment

Use this for source links, caveats, parameter details, longer checklists, or "not claiming this is universal" notes. Keep details here instead of overloading the main post.

## Internal Notes

- Longer mini-guide version: 250-450 words, use no more than 1-2 times per week.
- Deep tutorial version: 500-900 words, use only when the topic needs visuals, screenshots, or a serious walkthrough.
- Avoid tables in daily Reddit main posts unless the subreddit clearly favors technical long-form posts.
- For Reddit cadence, prefer five smaller useful posts over one overloaded weekly essay.

## What I noticed

## Why it happens

## A practical checklist

## Sources / context

## Question for the community
```

## Discord Column Plan

```markdown
# Discord Column: [name]

- Channel:
- Cadence:
- Host goal:
- User prompt:
- Participation template:
- Moderator notes:
- Source prep:
- Archive/follow-up:
```

## Short-Video Script

```markdown
# Short Video: [title]

- Platform:
- Duration:
- Audience:
- Hook:

| Time | Visual | Voiceover | On-screen text |
|---|---|---|---|
| 0-2s |  |  |  |
| 3-10s |  |  |  |
| 11-25s |  |  |  |
| 26-35s |  |  |  |

## Materials

## Source-backed Claims

## Cutdown Variants
```
