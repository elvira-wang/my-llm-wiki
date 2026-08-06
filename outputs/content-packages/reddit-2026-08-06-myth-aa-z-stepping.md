---
title: "Anti-aliasing is not a magic eraser for every layer line"
created: 2026-08-06
mode: daily-publishing-package
platform: reddit
channel: official-subreddit
column: Slicer Myth
signal_id: sig-reddit-aa-z-stepping
topic_package_id: topic-reddit-chitubox-weekly-2026-08-03
topic_package_file: outputs/topic-packages/reddit-chitubox-weekly-topics-2026-08-03.md
calendar_slot_id: reddit-2026-08-06-myth-aa-z-stepping
calendar_file: outputs/content-calendars/reddit-chitubox-2-week-trial-calendar-2026-08-03.md
scheduled_time: "2026-08-06 21:30 Beijing / 09:30 ET"
status: draft
post_url:
source_url: "https://www.reddit.com/r/ElegooMars/comments/1ux5c0j/any_advice_for_these_sorts_of_layer_lines/"
---

# Daily Publishing Package: AA vs Z-Stepping

## Publish Time

北京时间：2026-08-06 21:30

美国东部时间：2026-08-06 09:30 ET

## Brief

- Channel: CHITUBOX official subreddit
- Audience: Resin printing users tuning surface quality, especially miniature painters and returning resin users
- Goal: Myth-busting + support deflection by helping users diagnose whether visible lines are AA, orientation, layer height, or resolution
- Signal ID: `sig-reddit-aa-z-stepping`
- Topic package: `topic-reddit-chitubox-weekly-2026-08-03`
- Calendar slot: `reddit-2026-08-06-myth-aa-z-stepping`
- Thesis: Anti-aliasing helps soften XY pixel/edge artifacts, but it cannot remove every Z-layer step caused by layer height and surface angle.
- Recommended format: Original daily post + first comment with a practical triage checklist

## Recommended Title

Anti-aliasing is not a magic eraser for every layer line

## Title Options

1. Anti-aliasing is not a magic eraser for every layer line
2. Before you tune AA, check whether the lines are actually Z-stepping
3. AA, layer height, or orientation? A quick surface-line triage

## Daily Post

```markdown
Anti-aliasing can help resin prints, but it is not a magic eraser for every visible line.

A useful split:

- **XY pixel/edge texture**: AA and blur can soften the edge transition.
- **Z-layer stepping**: orientation, layer height, and local surface angle usually matter more.

If the lines show up on flatter plates, shallow curves, capes, weapons, or rounded peaks, you may be looking at Z-stepping rather than only an AA problem.

That does not mean AA is useless. It means AA should be one tool in the surface-quality workflow, not the first and only diagnosis.

My quick order would be:

1. Check orientation and whether the problem surface is too close to horizontal.
2. Check layer height.
3. Then tune AA / image blur for pixel texture and edge softness.

When you see surface lines, what do you check first: AA settings, angle, layer height, or screen resolution?
```

## Optional First Comment

```markdown
Source/context: inspired by a Reddit troubleshooting thread where a returning Mars 2 Pro user was getting visible stepping on minis and wondered whether anti-aliasing, CHITUBOX/Lychee, or XY pixel resolution was the answer.

The useful distinction:

- XY pixel texture comes from the LCD pixel grid and edge transitions. AA / grayscale / blur can help here, but too much blur can also soften fine details.
- Z-stepping comes from the model being built layer by layer. If a surface is shallow or close to horizontal, each layer can become visibly separated. AA cannot change the actual Z height between layers.
- Pre-supported orientation is not automatically the best orientation for your printer, layer height, and target surface quality.

Not saying "never use AA." More like: diagnose the direction of the artifact first, then choose the tool.

Original discussion:
https://www.reddit.com/r/ElegooMars/comments/1ux5c0j/any_advice_for_these_sorts_of_layer_lines/
```

## Evidence

| Claim | Confidence | Source |
|---|---|---|
| The source user saw visible stepping on flat faces, plates, rounded areas, and a cape while printing at 0.03mm on a Mars 2 Pro. | anecdotal | `raw/reddit/Any advice for these sorts of layer lines.md` |
| The thread split the diagnosis between anti-aliasing suggestions and comments pointing to orientation/Z-stepping. | anecdotal / debate | `raw/reddit/Any advice for these sorts of layer lines.md`, `digest/Any advice for these sorts of layer lines.md` |
| AA primarily helps XY pixel/edge transitions and cannot remove all Z-layer stepping. | consensus | `wiki/anti-aliasing.md`, `wiki/resin-z-stepping.md` |
| Z-stepping depends on layer height and surface angle; orientation can reduce or move visible stepping. | consensus | `wiki/resin-z-stepping.md`, `wiki/print-orientation-resin.md` |
| AA / blur settings can trade smoother edges for softer fine details. | consensus | `wiki/anti-aliasing.md` |

## Materials

- Wiki: `wiki/anti-aliasing.md`, `wiki/resin-z-stepping.md`, `wiki/print-orientation-resin.md`, `wiki/pixel-texture.md`
- Digest: `digest/Any advice for these sorts of layer lines.md`
- Raw: `raw/reddit/Any advice for these sorts of layer lines.md`
- Visual assets: optional CHITUBOX screenshots showing the same surface at different orientations; avoid using Reddit user images unless permission is available

## Outline

1. Hook: AA helps, but it is not a universal layer-line eraser.
2. Misbelief: every visible line is an AA/resolution issue.
3. Mechanism: separate XY pixel texture from Z-layer stepping.
4. Practical workflow: diagnose orientation/layer height first, then tune AA/blur.
5. CTA: ask the community which variable they check first.

## Comment-Seeding Questions

- What visual clues tell you a line is Z-stepping rather than XY pixel texture?
- Do you re-orient pre-supported files when the visible surface matters?
- What AA / blur settings have been reliable on your printer?
- When is post-processing easier than chasing a slicer setting?

## Reuse

- Reddit: Use the Daily Post as the main post; use Optional First Comment for the longer diagnostic distinction.
- Discord: Run a "diagnose the artifact" thread where users label photos as AA / angle / layer height / resolution / post-processing.
- Short video: Show "AA on, stepping still visible" as the hook, then compare a shallow surface vs a re-oriented surface.

## Accuracy Notes

- Do not frame AA as useless. The correct claim is that AA has a boundary: it helps XY edge/pixel texture more than Z-layer stepping.
- Do not claim one universal angle fixes every model. Orientation is a tradeoff with support placement, print time, and detail protection.
- Do not overstate the Reddit thread as a confirmed fix; it is a diagnostic discussion.
- Avoid making this a CHITUBOX vs Lychee comparison. The post should teach the artifact distinction, not software tribalism.
