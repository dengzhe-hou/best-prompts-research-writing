---
name: rebuttal
description: "Submission rebuttal pipeline. Parses external reviews, enforces coverage and grounding, drafts a safe text-only rebuttal under venue limits."
---

# Rebuttal Pipeline

> Abridged from: [wanshuiyin/Auto-claude-code-research-in-sleep · rebuttal](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/rebuttal/SKILL.md) (MIT, Copyright (c) 2026 wanshuiyin)
> The upstream external reviewer (Codex MCP), state file and command-line options were removed. The "External reviewer" in Phase 6 is the running model re-reading the draft critically; no second model is called. Name the venue and character limit in your message.

## Overview

This skill prepares a grounded, venue-compliant rebuttal for external reviews.

## Safety Model

Three hard gates — if any fails, do NOT finalize:

1. **Provenance gate** — every factual statement maps to: paper, review, user_confirmed_result, or future_work. No source = blocked.
2. **Commitment gate** — every promise maps to: already_done, approved_for_rebuttal, or future_work_only. Not approved = blocked.
3. **Coverage gate** — every reviewer concern ends in: answered, deferred_intentionally, or needs_user_input. No issue disappears.

## Workflow

### Phase 0: Resume or Initialize
Load paper, reviews, venue rules, any user-confirmed evidence.

### Phase 1: Validate Inputs and Normalize Reviews
Normalize all reviewer text into raw format.

### Phase 2: Atomize and Classify Reviewer Concerns
Create issue board with:
- issue_id (e.g., R1-C2)
- reviewer, round, raw_anchor
- issue_type: assumptions / theorem_rigor / novelty / empirical_support / clarity / other
- severity: critical / major / minor
- response_mode: direct_clarification / grounded_evidence / narrow_concession / etc.

### Phase 3: Build Strategy Plan
- Identify 2-4 global themes
- Choose response mode per issue
- Build character budget
- Identify blocked claims

### Phase 4: Draft Initial Rebuttal
Structure:
1. Short opener — thank reviewers + global resolutions
2. Per-reviewer numbered responses — answer → evidence → implication
3. Short closing — resolved / remaining / acceptance case

### Phase 5: Safety Validation
Run all lints:
- Coverage — every issue maps to draft anchor
- Provenance — every factual sentence has source
- Commitment — promises are approved
- Tone — flag aggressive/submissive phrases
- Limit — exact character count

### Phase 6: Stress Test
External reviewer checks for:
- Unanswered or weakly answered concerns
- Unsupported factual statements
- Risky or unapproved promises
- Tone problems

### Phase 7: Finalize
Output:
- `PASTE_READY.txt` — strict version, exact character count
- `REBUTTAL_DRAFT_rich.md` — extended version with more detail

## Key Rules

- **Never fabricate.** No invented evidence, numbers, derivations, citations.
- **Never overpromise.** Only promise what user explicitly approved.
- **Full coverage.** Every reviewer concern tracked and accounted for.
- **Evidence > rhetoric.** Derivations and numbers over prose.
- **Concede selectively.** Narrow honest concessions > broad denials.
- **Respect the limit.** Character budget is a hard constraint.
