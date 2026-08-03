---
name: content-signal-pipeline
description: Turn raw ideas, user-provided material, Reddit/community discussions, wiki notes, digests, raw sources, and web research into channel-ready content strategy packages and drafts for this LLM wiki/content factory. Use when asked to generate content ideas, Reddit posts, Discord column plans, short-video topics/scripts, weekly trend reports, source-backed campaign angles, or any workflow from idea/signal to publishable output using the project's knowledge base.
---

# Content Signal Pipeline

## Purpose

Use this skill to convert a loose idea or external signal into a source-backed content package for the project's business lines. Treat the repository as the content brain:

- `digest/INDEX.md` locates promising source analyses.
- `digest/` explains why raw materials work as content.
- `wiki/` provides verified reusable knowledge.
- `raw/` provides original cases, quotes, screenshots, comment patterns, and community language.
- Web search supplements current facts, platform context, and missing evidence when needed.

This skill is not only for Reddit. Use it for Reddit posts, Discord programming, short-video topics/scripts, tutorials, prompts, product copy, and other channel-specific outputs.

## Workflow

### 1. Define The Assignment

Identify:

- **Input type**: user idea, selected raw material, digest topic, weekly community trend, competitor/platform signal, or blank topic discovery.
- **Target channel**: Reddit, Discord, short video, tutorial, promo, changelog, or other.
- **Output depth**: topic shortlist, content package, final draft, or publishing calendar.
- **Business goal**: trust-building, community engagement, education, product adoption, feature feedback, lead generation, or support deflection.

If the user does not specify a channel, produce a cross-channel content package with Reddit, Discord, and short-video adaptations.

### 2. Build A Signal Map

Read sources in this order:

1. `digest/INDEX.md` for candidate briefs by topic, form, technique, and quality.
2. Relevant `digest/*.md` briefs for content angles and expression techniques.
3. Relevant `wiki/*.md` notes for factual grounding and internal links.
4. Relevant `raw/*` files for concrete cases, community language, images, comment disputes, and first-hand claims.
5. Web search only when facts are current, missing, external, or the user explicitly asks for latest/current research.

Never invent technical claims. Label evidence strength:

- `established`: physical mechanism or strongly verified fact.
- `consensus`: multiple sources/community agreement.
- `anecdotal`: one thread, creator, or user report.
- `debate`: active disagreement or contradictory evidence.
- `speculative`: plausible but not verified.

### 3. Extract Content Signals

For each promising source, extract:

- **User pain**: what failed, confused, annoyed, or surprised the audience.
- **Trigger scene**: the concrete situation a user would recognize.
- **Misbelief**: what the audience likely assumes incorrectly.
- **Mechanism**: why the issue happens, grounded in wiki or source evidence.
- **Community tension**: disagreement, myth, workaround, or surprising correction.
- **Resolution**: fix, checklist, diagnostic path, or unresolved question.
- **Reusable assets**: screenshots, images, quote snippets, parameter tables, links, model/setup details.
- **Content promise**: what the audience will be able to do/understand after consuming the piece.

Prefer threads with one of these patterns:

- Problem -> diagnosis -> confirmed fix.
- Strong misconception -> expert correction.
- High-comment controversy -> balanced explanation.
- Specific parameter/settings struggle -> reproducible checklist.
- Visual before/after -> easy demonstration.

### 4. Score And Select Angles

Score each angle from 1-5:

- **Audience urgency**: how painful or frequent the problem is.
- **Knowledge leverage**: how well the wiki can explain it.
- **Community fit**: whether the channel welcomes this kind of post.
- **Product fit**: whether CHITUBOX or the project can naturally help without forced promotion.
- **Evidence quality**: whether sources are strong enough for a confident post.
- **Asset availability**: whether there are images, quotes, examples, or steps.

Select 1-3 angles. Reject angles that require unverifiable claims, overreach beyond the evidence, or read like disguised advertising in community spaces.

### 5. Choose Channel Form

Read only the relevant reference:

- Reddit output: `references/platform-playbooks.md#reddit`
- Discord output: `references/platform-playbooks.md#discord`
- Short-video output: `references/platform-playbooks.md#short-video`
- Cross-channel package: read all relevant sections.
- Final formatting and deliverables: `references/output-templates.md`

Adapt the same angle by changing the participation mode:

- Reddit: lead with a useful question, field note, or mini-guide; cite sources transparently; avoid corporate tone.
- Discord: turn the topic into a recurring prompt, live help thread, challenge, office-hours topic, or FAQ seed.
- Short video: convert the mechanism into a visual hook, one mistake, one fix, and a tight demo.

### 6. Produce The Content Package

Unless the user asks for only a brainstorm, include:

- Recommended title/topic.
- Target channel and audience.
- One-sentence thesis.
- Why this should work now.
- Evidence table with source paths/URLs and confidence.
- Material list: raw files, wiki notes, digest briefs, external links, images/screenshots to use.
- Content outline.
- Platform-specific draft or script.
- Safety/accuracy notes.
- Follow-up variants for other channels.

For repository output tasks, write files under `outputs/`:

- `outputs/promos/` for promotional copy.
- `outputs/tutorials/` for tutorials.
- `outputs/content-packages/` for strategy packages, Reddit posts, Discord programming, and short-video plans.

Create the subfolder if needed. Use lowercase, descriptive filenames.

## Quality Rules

- Ground technical explanations in `wiki/` first; use `raw/` for lived examples and language.
- Keep Reddit quotations short and attributed to the raw file/source URL.
- Distinguish "the community suggested" from "the fix was confirmed."
- Do not present a single Reddit comment as product truth.
- For current trends, use web search and include accessed/source URLs.
- For community posts, make the brand useful before it is visible. The post should survive even if all brand mentions are removed.
- Prefer "diagnostic checklists" over generic advice.
- Include "what would change my mind" or "where this may fail" when the evidence is debated.

## CHITUBOX Project Defaults

When the user references CHITUBOX without more context, assume:

- Core audience: resin printing users, from advanced beginners to serious hobbyists.
- Strong topics: supports, orientation, hollowing, drain holes, suction, exposure calibration, anti-aliasing, surface quality, file repair, workflow mistakes.
- Product posture: helpful slicer/workflow expert, not hard-sell brand voice.
- Best content shape: community case -> mechanism -> Chitubox workflow/checklist -> invite users to compare settings or share failed cases.

Use these assumptions only as defaults; override them when the user's brief is more specific.
