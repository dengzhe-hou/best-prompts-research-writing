---
name: idea-discovery
description: "Full idea discovery pipeline. Orchestrates literature survey → idea generation → novelty check → review to go from a broad research direction to validated ideas."
---

# Idea Discovery Pipeline

> Abridged from: [wanshuiyin/Auto-claude-code-research-in-sleep · idea-discovery](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/idea-discovery/SKILL.md) (MIT, Copyright (c) 2026 wanshuiyin)
> This short version omits the upstream cross-model review, pilot experiments and checkpoints, and it calls sub-skills (/idea-creator, /novelty-check, /research-review) that are not included here. Install the upstream version for the full workflow.

## Overview

This skill chains sub-skills into a single automated pipeline:

```
/research-lit → /idea-creator → /novelty-check → /research-review
  (survey)      (brainstorm)    (verify novel)    (critical feedback)
```

## Workflow

### Phase 1: Literature Survey
Search arXiv, Google Scholar, Semantic Scholar for recent papers. Build a landscape map: sub-directions, approaches, open problems. Identify structural gaps and recurring limitations.

### Phase 2: Idea Generation
Brainstorm 8-12 concrete ideas. Filter by feasibility, compute cost, quick novelty search. Rank by empirical signal.

### Phase 3: Deep Novelty Verification
For each top idea, run a thorough novelty check:
- Multi-source literature search (arXiv, Scholar, Semantic Scholar)
- Cross-verify with LLM
- Check for concurrent work (last 3-6 months)
- Identify closest existing work and differentiation points

### Phase 4: External Critical Review
Get brutal feedback from a senior reviewer perspective:
- Score the idea
- Identify weaknesses
- Suggest minimum viable improvements
- Provide concrete feedback on experimental design

## Key Rules

- **Don't skip phases.** Each phase filters and validates — skipping leads to wasted effort later.
- **Kill ideas early.** Better to kill 10 bad ideas than to implement one and fail.
- **Empirical signal > theoretical appeal.** An idea with a positive pilot outranks a "sounds great" idea without evidence.
- **Document everything.** Dead ends are just as valuable as successes for future reference.

## Output

```markdown
# Idea Discovery Report

## Executive Summary
[2-3 sentences: best idea, key evidence, recommended next step]

## Literature Landscape
[from Phase 1]

## Ranked Ideas
[from Phase 2, updated with Phase 3-4 results]

### 🏆 Idea 1: [title] — RECOMMENDED
- Novelty: CONFIRMED
- Reviewer score: X/10
- Next step: implement full experiment

## Eliminated Ideas
[ideas killed at each phase, with reasons]
```
