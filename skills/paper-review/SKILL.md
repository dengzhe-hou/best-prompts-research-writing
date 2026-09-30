---
name: paper-review
description: "Critical review of a paper draft or research idea by the running model, in a single pass. Use when user says 'review my paper', 'review my draft', 'review my idea', 'critique this', 'feedback on research'."
---

# Research Review

> Adapted from: [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/research-review/SKILL.md) research-review and the external-review phase of idea-discovery (MIT, Copyright (c) 2026 wanshuiyin). The review dimensions and output template were added here.
> This version does not call a second model: the running model acts as the reviewer, in a single round.

## Overview

This skill provides critical feedback on a paper draft or a research idea.

## Review Protocol

### Phase 1: Load Context
- Read the paper draft, or the idea/proposal
- Understand the claims, methodology, and results (expected results for an idea)

### Phase 2: Critical Review
Act as a senior reviewer (NeurIPS/ICML level):
- Score the work (1-10)
- Identify weaknesses
- Suggest minimum viable improvements
- Provide concrete feedback on experimental design

### Phase 3: Synthesize Feedback
- Categorize issues by severity (critical/major/minor)
- Provide actionable recommendations
- Highlight strengths and opportunities

## Review Dimensions

1. **Novelty**: Is this truly new? What's the closest existing work?
2. **Significance**: Does this matter? Who benefits?
3. **Soundness / Feasibility**: For a paper, do the results support the claims? For an idea, can it be done with available resources?
4. **Experimental Design**: Are the experiments well-designed?
5. **Writing Quality**: Is the work clearly communicated?

## Output Format

```markdown
## Review Summary

**Score**: X/10

### Strengths
- [strength 1]
- [strength 2]

### Weaknesses (Critical)
- [weakness 1]
- [weakness 2]

### Weaknesses (Major)
- [weakness 3]

### Weaknesses (Minor)
- [weakness 4]

### Recommendations
1. [recommendation 1]
2. [recommendation 2]

### Minimum Viable Improvements
- [improvement 1]
- [improvement 2]
```

## Key Rules

- Be honest and constructive
- Focus on substance, not style
- Provide actionable feedback
- Distinguish between critical and minor issues
- Acknowledge strengths as well as weaknesses
