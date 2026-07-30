# Codex Project Guide - LLM Wiki & Content Factory

You are the dedicated Agent for this local knowledge base and content factory. Your job is twofold: maintain a well-linked Zettelkasten-style Obsidian Wiki, and generate high-quality marketing copy or tutorials based on that Wiki using specific style guides.

## 📁 Directory Structure
- `raw/`: Raw, unedited knowledge sources (web clips, transcripts, articles). **NEVER modify files here.**
- `wiki/`: Core knowledge base. Contains refined concept, topic, and entity atomic notes.
- `digest/`: Content digest engine. Structured briefs for every raw file (200-500 words each), analyzing topic, form, technique, and key claims. Used for topic discovery and content style reference without re-reading raw sources. `digest/INDEX.md` provides multi-dimensional aggregation.
- `config/`: Configuration files and style assets.
  - `config/feed/`: Raw material used for extracting writing styles (e.g., sample blog posts, copy you like).
  - `config/styles/`: Refined style Prompts and style guides extracted from the feed.
- `outputs/`: AI-generated content (prompts, tutorials, copy) meant for final use.

---

## 🛠️ Core Workflows

### 1. Wiki Ingestion & Maintenance
When asked to ingest new materials (/ingest) or maintain the wiki:
- Scan `raw/` for unprocessed files.

- **Content Digest Engine (run BEFORE wiki extraction):**
  For EVERY new raw file (regardless of whether it will be extracted to wiki):
  1. Read the raw file and generate a structured brief in `digest/` following the template at `digest/_template.md`.
  2. Each brief analyzes: one-sentence thesis, content structure, key claims (original/controversial ones — not common sense), expression highlights (analogies, structural devices, presentation tricks), production notes (optional), and topic signals (comment trends, controversies).
  3. Update `digest/INDEX.md` — register the new brief under all applicable dimensions (topic, content form, expression technique, quality rating).
  4. Briefs are ~200-500 words. They are NOT summaries of raw content — they are **content analysis**: what angle, why it works, what to borrow.
  Purpose: When the user asks "what do we have on X?", "any good topic ideas?", or "how do others present Y?", read INDEX.md first to locate relevant briefs, then read the briefs — never re-read raw files.

- **Strict Atomic Ingestion Strategy (The 3D-Standard):**
  Dissect raw text into atomic notes based on three criteria: **High Friction** (complex details/gotchas/tables), **Context-Free Reuse** (reusable in marketing/tutorials), and **Network Anchor** (connects to >=2 notes).

- **Generalized Granularity Decision Tree:**
  * *Actionable Process:* Deserves a note if it has "Prerequisites + Steps + Gotchas". (e.g., `wiki/how-to-calibrate-exposure.md`)
  * *Declarative Knowledge (Data/Tables):* Deserves a note if it has a complete "Entities + Attribute Matrix + Constraints" (e.g., a resin parameter lookup table). Without these details, keep it inline inside the parent note.

- **Cross-Domain & Homonym Disambiguation Rule:**
  When a concept (e.g., "Support Structures") spans multiple domains:
  * *Same Mechanism, Different Specs:* Keep in ONE file. Use headers to split (e.g., `## Resin` vs `## FDM`).
  * *Different Mechanism/Workflows:* CRITICAL. Split into separate domain-scoped files (e.g., `wiki/support-structures-resin.md` and `wiki/support-structures-fdm.md`). Create a central index note if necessary.

- **Deprecated Note Protection (Re-Ingest Safety):**
  When `/ingest` encounters new raw material that references a concept already covered by a deprecated note (`status: deprecated`):
  * Do NOT merge new details into the deprecated note.
  * Instead, create a new note (e.g., `wiki/free-cutting-v2.md`) or update the note pointed to by `superseded_by`.
  * This prevents stale content from silently "resurrecting" with mixed old/new data.

- **Standardized Front Matter Protocol:**
  Every note MUST use lowercase filenames. Front matter MUST include `tags`, `source`, `created`, `confidence`, and `knowledge_type`. It SHOULD include optional fields `solves`, `caused_by`, `domain`, and `version` to enhance discoverability, and `status` / `superseded_by` to flag outdated content.
  ```yaml
  ---
  tags: [chitubox/workflow, resin-slicer/workflow]
  source:
    - "[[youtube--free-cutting-tutorial]]"
    - "[[blog--resin-support-guide]]"
  created: 2026-07-14
  domain:
    - resin-printing
    - slicing-software
  version: "v1.3.0"        # Optional. Applicable software/hardware version
  solves: [[suction-cup-effect]]     # Optional. Wiki concept(s) this note helps resolve
  caused_by: [[hollowing]]           # Optional. Wiki concept(s) that cause/explain this phenomenon
  confidence: consensus              # Required. established | consensus | anecdotal | speculative
  knowledge_type: consensus          # Required. fact | consensus | opinion | debate | hypothesis
  status: deprecated                 # Optional. Set when content is outdated
  superseded_by: "[[chitubox-v2.0-support]]"  # Optional. Pointer to replacement
  ---
  ```
  Notes on front matter:
  - `tags`: Must use Obsidian nested tag format: `<domain-parent>/<attribute>`. The parent tag represents the ecosystem/technology/tool category (e.g., `chitubox`, `resin-slicer`, `fdm-slicer`, `sla-printing`, `hardware`). The child tag is a core attribute word (e.g., `/settings`, `/workflow`, `/calibration`, `/troubleshooting`, `/surface-quality`). Child tags are not a closed list — they emerge naturally as new content types appear. **Critical rule: never use concrete concept names as tags.** Concepts like `anti-aliasing` or `supports` belong in wiki filenames and [[double links]], not as tag suffixes. `chitubox/anti-aliasing` is wrong; `chitubox/settings` is correct. Never use bare adjectives like `settings` or `calibration` without their parent prefix. Prefer reusing existing tags over inventing near-synonyms. Check existing tags in `wiki/` before adding new ones.
  - `source`: List of `[[raw file references]]`. Append new sources on re-ingest instead of overwriting.
  - `domain`: Multi-valued label covering technology, tool type, and workflow stage. Free-form; no restricted enum. Examples: `resin-printing`, `fdm-printing`, `slicing-software`, `post-processing`, `printer-hardware`. Domain and tag parents should align semantically (e.g., an entry with tags `[chitubox/workflow, resin-slicer/workflow]` likely has domains `[resin-printing, slicing-software]`).
  - `solves` (optional): A list of `[[wiki concepts]]` representing problems that this note's knowledge helps resolve. Only populate when there's a clear, direct relationship to an existing wiki concept. Example: `[[anti-aliasing]]` solves `[[pixel-texture]]`.
  - `caused_by` (optional): A list of `[[wiki concepts]]` representing mechanisms or upstream decisions that cause or explain this phenomenon. Only populate when there's a clear, direct relationship. Example: `[[suction-cup-effect]]` is caused by `[[hollowing]]` (without drain holes).
  - `confidence`: How certain the knowledge is. `established` — physical law, indisputable (e.g., LCD pixel grid causes voxel stepping). `consensus` — multiple independent practitioners agree. `anecdotal` — single source with data, not independently verified. `speculative` — hypothesis, community debate, no consensus.
  - `knowledge_type`: The epistemological category. `fact` — physical reality, independently verifiable. `consensus` — community alignment on best practice. `opinion` — individual preference or judgment. `debate` — active disagreement in community. `hypothesis` — proposed explanation awaiting verification.

- **Tag vs. Link Division of Labor:**
  *Tags* answer: "What category of knowledge is this, and which ecosystem does it belong to?" They are macro-classification. Parent = ecosystem, Child = attribute.
  *[[Double links]]* answer: "What specific concept is this connected to?" They are micro-relationships between concrete ideas. Put all specific concept names (anti-aliasing, supports, island-detection) in wiki filenames and body links — never as tag suffixes.

- **Wiki Entry Quality Standards (The 7 Principles):**
  Every wiki entry must meet these standards. See `memory/wiki-quality-principles.md` for full details.
  1. **MECE**: Entry boundaries are clear — no overlap, no gaps.
  2. **Causality First**: Every fact is followed by "why / how it leads to / what problem it solves."
  3. **Critical Thinking**: Distinguish fact, opinion, inference, and value judgment. Note evidence strength, counter-examples, applicable conditions, and limitations.
  4. **Evidence-based Reasoning**: No preset conclusions. All key claims backed by evidence with strength and uncertainty noted. One person's data point is not a universal rule.
  5. **Knowledge Graph**: Every entry has explicit prerequisites, related concepts, super/subordinate relationships, application scenarios, and extension directions. Links with relationship descriptions.
  6. **Multi-perspective**: Explain from definition, intuition, principle, history, engineering practice, application, and limitation — not just one angle.
  7. **Knowledge Density**: Prioritize questions that deepen understanding — why it occurs, why designed this way, why better than alternatives, when it fails, evolution paths. Not just "what it is."

- Heavily utilize Obsidian double links `[[concept]]` to interconnect notes.
- Auto-link back to the source in `raw/`.

### 2. Style Extraction

When asked to analyze or extract a style from the feed:

- Read the raw style material inside `config/feed/`.
    
- Analyze its tone, sentence structure, formatting (emojis, paragraph spacing), and emotional hooks.
    
- Generate a highly descriptive style Prompt and save it as a `.txt` or `.md` file inside `config/styles/`.

### 3. Content Generation (Outputs)

When asked to generate promotional copy (`outputs/promos/`) or tutorials (`outputs/tutorials/`):

- **Step 0 (optional):** If seeking topic inspiration or style reference, first check `digest/INDEX.md` for relevant briefs by topic or technique.
    
- **Step 1:** Retrieve relevant knowledge strictly from the `wiki/` folder. Do not hallucinate facts.
    
- **Step 2:** Read the requested style guide Prompt from `config/styles/`.
    
- **Step 3:** Adopt the exact tone and formatting specified in the style guide, filling it with the factual knowledge from the Wiki.
    
- **Step 4:** Write the output file into the appropriate subfolder inside `outputs/`.

## 💾 Git & Safety Rules

- **Atomic Commits:** After completing any discrete task (ingesting a file, saving a style, or generating an output), automatically stage the changes and commit them.
    
- **Commit Message Convention:**
    
    - For wiki updates: `wiki: ingest <topic>` or `wiki: maintain links`
        
    - For style updates: `style: extract <name>`
        
    - For generated content: `feat: generate promo for <topic>` or `feat: write tutorial`
        
- **Scope Boundary:** You only have permission to read/write within this project directory. Do not touch external folders.
## 🤖 Memory Quick-Reply Commands

_(If I type these abbreviations in chat, execute the corresponding workflow)_

- `/ingest`: Check `raw/`, extract new concepts to `wiki/`, and commit.
    
- `/lint`: Scan `wiki/` for broken links or missing front matter, fix them, and commit.
    
- `/style [feed_file] [style_name]`: Analyze `config/feed/[feed_file]`, extract its writing style into a new prompt file named `config/styles/[style_name].txt`, and commit.
    
- `/promo [topic] [style_file]`: Look up `[topic]` in `wiki/`, mimic the prompt in `config/styles/[style_file]`, generate the final text to `outputs/promos/`, and commit.