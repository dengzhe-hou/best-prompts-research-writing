[Project home](README_EN.md) | [中文 Skill 目录](SKILLS.md) | 🇺🇸 English skill catalog

---

# Research Writing Skill Catalog

> 8 installable agent skills for research, writing, and review. Each scenario has a primary candidate (included in this repository under `skills/`) and, where available, an alternative candidate (link only).

> Most included skills are short versions of upstream skills, about 7% to 22% the length of the May 2026 upstream versions. They are short, easy to read, and work once installed, but they do less than the originals, and some call sub-skills that are not included here. Each entry says what was removed and links to the original; install the original if you need the full workflow.

---

## Installation

`idea-discovery`, `research-lit`, `paper-writing` and `rebuttal` share their names with the originals in [ARIS](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep), and "install all" below would overwrite them. If you already have ARIS, use the second command to install only the other four.

**Claude Code**

```bash
git clone https://github.com/dengzhe-hou/best-prompts-research-writing.git
mkdir -p ~/.claude/skills

# Install all
for d in best-prompts-research-writing/skills/*/; do cp -R "${d%/}" ~/.claude/skills/; done

# Already have ARIS: install only the four with different names
for n in research-gap paper-review humanizer humanizer-zh-academic; do cp -R best-prompts-research-writing/skills/$n ~/.claude/skills/; done

# Install one, e.g. rebuttal
cp -R best-prompts-research-writing/skills/rebuttal ~/.claude/skills/
```

**Codex**: replace `~/.claude/skills` above with `~/.codex/skills`.

**Cursor**: loads skills from `~/.claude/skills/` and `~/.codex/skills/`, so either install above works.

After installing, call a skill with `/skill-name` in Claude Code and Cursor (for example `/rebuttal`); in Codex, type `$rebuttal` or pick it from `/skills`. You can also just describe the task in your message.

---

## 📌 Quick Navigation

| Stage | Scenarios |
|---|---|
| Research | [1.1 Idea Discovery](#11-idea-discovery) · [1.2 Literature Review](#12-literature-review) · [1.3 Research Gap](#13-research-gap) |
| Writing | [2.1 Paper Writing](#21-paper-writing) · [2.2 De-AI English](#22-de-ai-english) · [2.3 De-AI Chinese](#23-de-ai-chinese) |
| Review | [3.1 Paper Review](#31-paper-review) · [3.2 Rebuttal](#32-rebuttal) |

---

# I. Research

## 1.1 Idea Discovery

### Primary candidate: `idea-discovery`

> Source: abridged from [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/idea-discovery/SKILL.md) (MIT), about 16% of the May upstream version

**What it does**: four steps (literature survey, idea generation, novelty check, review), ending with a ranked idea report.

**Note**: it calls three sub-skills, `/idea-creator`, `/novelty-check` and `/research-review`, which are not included here. The upstream cross-model review, pilot experiments and checkpoints were removed, so ideas are ranked on feasibility, novelty and expected impact without running experiments.

**File**: [`skills/idea-discovery/SKILL.md`](skills/idea-discovery/SKILL.md)

### Alternative (link only)

> [lishix520/academic-paper-skills](https://github.com/lishix520/academic-paper-skills) (MIT)

A framework for planning and writing academic papers.

---

## 1.2 Literature Review

### Primary candidate: `research-lit`

> Source: abridged from [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/research-lit/SKILL.md) (MIT), about 8% of the May upstream version

**What it does**: searches arXiv, Semantic Scholar and Google Scholar, de-duplicates, analyzes and synthesizes, and outputs a comparison table.

**Note**: the Zotero, Obsidian, DeepXiv, Exa, Gemini and OpenAlex sources listed in the file need upstream scripts or MCP servers that are not included here. The upstream Research Wiki was removed. Upstream added a step that checks whether each paper really exists on 2026-05-13, after this copy was made, so verify the papers it lists yourself.

**File**: [`skills/research-lit/SKILL.md`](skills/research-lit/SKILL.md)

### Alternative (link only)

> [Weizhena/Deep-Research-skills](https://github.com/Weizhena/Deep-Research-skills) (MIT)

Structured deep research in three steps (outline, research, report) with human checkpoints.

---

## 1.3 Research Gap

### Primary candidate: `research-gap`

> Source: written for this collection; no upstream counterpart

**What it does**: looks for methodological, theoretical, empirical and application gaps, assesses importance and feasibility, and outputs a structured report.

**File**: [`skills/research-gap/SKILL.md`](skills/research-gap/SKILL.md)

### Alternative (link only)

> [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) (CC BY-NC 4.0)

A full research, writing, review, revision and finalization workflow.

---

# II. Writing

## 2.1 Paper Writing

### Primary candidate: `paper-writing`

> Source: abridged from [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/paper-writing/SKILL.md) (MIT), about 7% of the May upstream version

**What it does**: lists five phases: planning, figures, LaTeX writing, compilation, and an improvement loop.

**Note**: this short version is closer to an outline. Every phase calls a sub-skill (`/paper-plan`, `/paper-figure`, `/paper-write`, `/paper-compile`, `/auto-paper-improvement-loop`), none of which is included here, and the upstream cross-model review and assurance gate were removed. The file sets `AUTO_PROCEED = true`, so it does not pause between phases; ask it to stop after each phase if you want to review. Install the original to actually write a paper with it.

**File**: [`skills/paper-writing/SKILL.md`](skills/paper-writing/SKILL.md)

### Alternative (link only)

> [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills) (MIT)

For ML, CV and NLP papers, adapted from Prof. Peng Sida's public notes.

---

## 2.2 De-AI English

### Primary candidate: `humanizer`

> Source: abridged from [blader/humanizer](https://github.com/blader/humanizer/blob/main/SKILL.md) (MIT), about 10% of the May upstream version

**What it does**: detects 11 kinds of AI-writing patterns based on Wikipedia's "Signs of AI writing" (the May upstream version has 29), rewrites, then checks the result for remaining tells.

**Note**: the one-line "Fix" note under each pattern was added here.

**File**: [`skills/humanizer/SKILL.md`](skills/humanizer/SKILL.md)

### Alternative (link only)

> [matsuikentaro1/humanizer_academic](https://github.com/matsuikentaro1/humanizer_academic) (MIT)

Based on humanizer, for medical papers.

---

## 2.3 De-AI Chinese

### Primary candidate: `humanizer-zh-academic`

> Source: abridged from [redbaronyyyyy-eng/humanizer-zh-academic](https://github.com/redbaronyyyyy-eng/humanizer-zh-academic/blob/main/SKILL.md) (MIT), about 22% of the upstream file

**What it does**: detects 6 AI-writing patterns in Chinese academic text (upstream has 16), rewrites following a fixed procedure, and self-scores. Upstream aims to lower AIGC detection rates; this repository has not tested that.

**File**: [`skills/humanizer-zh-academic/SKILL.md`](skills/humanizer-zh-academic/SKILL.md)

---

# III. Review

## 3.1 Paper Review

### Primary candidate: `paper-review`

> Source: adapted from research-review and the external-review phase of idea-discovery in [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/research-review/SKILL.md) (MIT); the review dimensions and output template were added here

**What it does**: reviews a paper draft or a research idea on novelty, significance, soundness (feasibility for an idea), experimental design and writing quality, lists issues by severity, and gives a 1 to 10 score.

**Note**: no second model is called. The running model acts as the reviewer, in a single round.

**File**: [`skills/paper-review/SKILL.md`](skills/paper-review/SKILL.md)

### Alternative (link only)

> [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) (CC BY-NC 4.0)

Includes review and revision workflows.

---

## 3.2 Rebuttal

### Primary candidate: `rebuttal`

> Source: abridged from [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/rebuttal/SKILL.md) (MIT), about 14% of the May upstream version

**What it does**: breaks down reviewer comments, plans a response strategy, and drafts within a character limit. Three safety gates: every factual statement needs a source; every promise is either already done, approved by you, or stated as future work; every reviewer concern is accounted for. No invented data or citations.

**Note**: the upstream external reviewer model, state file and command-line options were removed. The "External reviewer" in Phase 6 is the running model; no second model is called. State the venue and character limit in your message.

**File**: [`skills/rebuttal/SKILL.md`](skills/rebuttal/SKILL.md)

---

# Sources and Licenses

| Upstream | License | Included here |
|---|---|---|
| [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) | [MIT](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/LICENSE), Copyright (c) 2026 wanshuiyin | `idea-discovery`, `research-lit`, `paper-writing`, `paper-review`, `rebuttal` |
| [blader/humanizer](https://github.com/blader/humanizer) | [MIT](https://github.com/blader/humanizer/blob/main/LICENSE), Copyright (c) 2025 Siqi Chen | `humanizer` |
| [redbaronyyyyy-eng/humanizer-zh-academic](https://github.com/redbaronyyyyy-eng/humanizer-zh-academic) | [MIT](https://github.com/redbaronyyyyy-eng/humanizer-zh-academic/blob/main/LICENSE), Copyright (c) 2025 redbaronyyyyy-eng | `humanizer-zh-academic` |

This repository's abridgements and adaptations of these skills are released under MIT; see [`skills/LICENSE`](skills/LICENSE). Alternatives are linked, not copied.

# Suggesting a Skill

Suggestions are welcome. Please name the source repository and license, and say whether the skill is verbatim, abridged, or original. Only MIT or compatibly licensed skills are copied into this repository; others are linked.

Last reviewed: 2026-09-30
