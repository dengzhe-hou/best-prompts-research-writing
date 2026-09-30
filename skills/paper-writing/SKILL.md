---
name: paper-writing
description: "Outline of the ARIS paper-writing pipeline (plan → figures → LaTeX → compile → improve). Needs the ARIS sub-skills /paper-plan, /paper-figure, /paper-write, /paper-compile and /auto-paper-improvement-loop, which are not included here."
---

# Paper Writing Pipeline

> Abridged from: [wanshuiyin/Auto-claude-code-research-in-sleep · paper-writing](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/paper-writing/SKILL.md) (MIT, Copyright (c) 2026 wanshuiyin)
> This short version is an outline: each phase calls sub-skills (/paper-plan, /paper-figure, /paper-write, /paper-compile, /auto-paper-improvement-loop) that are not included here, and the upstream reviewer model and assurance gate were removed. Install the upstream version to run it.

## Overview

This skill chains sub-skills into a single automated pipeline:

```
/paper-plan → /paper-figure → /paper-write → /paper-compile → /auto-paper-improvement-loop
  (outline)     (plots)        (LaTeX)        (build PDF)       (review & polish)
```

## Constants

- **VENUE = `ICLR`** — Target venue (ICLR, NeurIPS, ICML, CVPR, ACL, AAAI, ACM, IEEE)
- **MAX_IMPROVEMENT_ROUNDS = 2** — Review→fix→recompile rounds
- **AUTO_PROCEED = true** — Auto-continue between phases

## Pipeline

### Phase 1: Paper Plan
Create structural outline:
- Parse narrative report for claims, evidence, figures
- Build Claims-Evidence Matrix
- Design section structure (5-8 sections)
- Plan figure/table placement

### Phase 2: Figure Generation
Generate data-driven plots and tables:
- Read figure plan from outline
- Generate matplotlib/seaborn plots
- Generate LaTeX comparison tables

### Phase 3: LaTeX Writing
Generate section-by-section LaTeX:
- Write each section following the plan
- Insert figure/table references
- Build references.bib
- De-AI polish

### Phase 4: Compilation
Build the PDF:
- `latexmk -pdf` with automatic multi-pass
- Auto-fix common errors
- Post-compilation checks

### Phase 5: Auto Improvement Loop
Polish the paper (2 rounds):
- Round 1: Review full paper → identify issues → implement fixes → recompile
- Round 2: Re-review with context → identify remaining issues → fix → recompile

## Key Rules

- **Don't skip phases.** Each phase builds on the previous one.
- **Compilation must succeed** before entering the improvement loop.
- **Preserve all PDFs.** The user needs round0/round1/round2 for comparison.
- **Respect page limits.** If the paper exceeds the venue limit, suggest specific cuts.

## Typical Timeline (upstream pipeline with all sub-skills installed)

| Phase | Duration |
|-------|----------|
| 1. Paper Plan | 5-10 min |
| 2. Figures | 5-15 min |
| 3. LaTeX Writing | 15-30 min |
| 4. Compilation | 2-5 min |
| 5. Improvement | 15-30 min |

**Total: ~45-90 min** for a full paper from narrative report to polished PDF, when run with the upstream sub-skills.
