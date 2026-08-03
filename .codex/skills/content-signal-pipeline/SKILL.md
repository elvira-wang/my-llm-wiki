---
name: content-signal-pipeline
description: Turn raw ideas, user-provided material, Reddit/community discussions, wiki notes, digests, raw sources, web research, and business goals into signal boards, content calendars, and channel-ready content packages for this LLM wiki/content factory. Use when asked to generate content ideas, Reddit posts, Discord column plans, short-video topics/scripts, weekly trend reports, source-backed campaign angles, content calendars, trial calendars, or any workflow from idea/signal to publishable output using the project's knowledge base.
---

# Content Signal Pipeline

## Purpose

Use this skill to convert loose ideas, external signals, or knowledge-base material into source-backed content planning and publishing assets for the project's business lines.

The pipeline has three modes:

1. `signal-board`: turn raw/digest/wiki/web/business goals into a ranked board of content signals.
2. `calendar`: turn a signal board into a 1-2 week content calendar with slots, columns, timing, and goals.
3. `content-package`: turn one calendar slot or selected signal into a publishable post/script/package.

Treat the repository as the content brain:

- `digest/INDEX.md` locates promising source analyses.
- `digest/` explains why raw materials work as content.
- `wiki/` provides verified reusable knowledge.
- `raw/` provides original cases, quotes, screenshots, comment patterns, and community language.
- Web search supplements current facts, platform context, and missing evidence when needed.

This skill is not only for Reddit. Use it for Reddit posts, Discord programming, short-video topics/scripts, tutorials, prompts, product copy, and other channel-specific outputs.

## Mode Selection

Choose the mode from the user's wording:

- Use `signal-board` when the user asks what topics/signals are worth doing, what the content calendar should be based on, what this week's community trends are, or asks for upstream topic discovery.
- Use `calendar` when the user asks for a content calendar, trial calendar, posting cadence, column plan, or schedule. If no relevant signal board exists, generate or update a signal board first.
- Use `content-package` when the user asks to write today's post, generate a Reddit/Discord/short-video draft, or produce the asset pack for a specific date, slot, or topic.
- If the user asks for an end-to-end workflow, produce artifacts in this order: signal board -> calendar -> content package.

Use stable IDs to connect artifacts:

- `signal_id`: one reusable content opportunity, such as `sig-reddit-fep-release-film`.
- `calendar_slot_id`: one scheduled publishing slot, such as `reddit-2026-08-03-case-fep`.
- `package_file`: the content package generated for a slot.

Every calendar slot should cite a `signal_id`. Every content package generated from a calendar should cite `calendar_slot_id`, `signal_id`, and `calendar_file` in frontmatter.

## Workflow

### 1. Define The Assignment

Identify:

- **Input type**: user idea, selected raw material, digest topic, weekly community trend, competitor/platform signal, or blank topic discovery.
- **Target channel**: Reddit, Discord, short video, tutorial, promo, changelog, or other.
- **Output depth/mode**: signal board, topic shortlist, content calendar, content package, final draft, or publishing calendar.
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

For `signal-board` mode, keep all credible candidate signals and rank them. For `calendar` and `content-package` modes, select only the angles needed for the requested slots or drafts. Reject angles that require unverifiable claims, overreach beyond the evidence, or read like disguised advertising in community spaces.

### 5. Build Or Use The Planning Artifact

For `signal-board` mode:

- Create `outputs/content-signals/` if needed.
- Write a lowercase descriptive signal board file.
- Include candidate signals, scores, evidence, wiki support, platform fit, risk, and recommended next action.

For `calendar` mode:

- Read the relevant signal board first when available.
- If no signal board exists, create one before the calendar unless the user explicitly asks for a quick calendar only.
- Create `outputs/content-calendars/` if needed.
- Each slot must include `calendar_slot_id`, `signal_id`, date, time, column, format, title, source base, package file, status, and CTA.

For `content-package` mode:

- Read the requested calendar slot when available.
- Use the slot's `signal_id`, source base, column, and format as constraints.
- Create `outputs/content-packages/` if needed.
- Include frontmatter linking back to `calendar_slot_id`, `signal_id`, and `calendar_file`.

### 6. Choose Channel Form

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

### 7. Produce The Output

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
- `outputs/content-signals/` for signal boards.
- `outputs/content-calendars/` for calendars and trial calendars.
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
