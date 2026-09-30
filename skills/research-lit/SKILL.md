---
name: research-lit
description: "Search and analyze research papers, find related work, summarize key ideas. Use when user says 'find papers', 'related work', 'literature review'."
---

# Research Literature Review

> Abridged from: [wanshuiyin/Auto-claude-code-research-in-sleep · research-lit](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/research-lit/SKILL.md) (MIT, Copyright (c) 2026 wanshuiyin)
> The Zotero, Obsidian, DeepXiv, Exa, Gemini and OpenAlex sources need upstream scripts or MCP servers that are not included here. Install the upstream version for those and for the Research Wiki.

## Overview

This skill searches multiple sources to find and analyze research papers on a given topic.

## Data Sources

| Priority | Source | What it provides |
|----------|--------|-----------------|
| 1 | Zotero (via MCP) | Collections, tags, annotations, BibTeX |
| 2 | Obsidian (via MCP) | Research notes, paper summaries |
| 3 | Local PDFs | Raw PDF content |
| 4 | Web search | arXiv, Semantic Scholar, Google Scholar |
| 5 | Semantic Scholar API | Published venue papers (IEEE, ACM) |
| 6 | DeepXiv CLI | Progressive paper retrieval |
| 7 | Exa Search | AI-powered broad web search |
| 8 | Gemini | AI-powered broad discovery |
| 9 | OpenAlex | Open citation graph |

## Workflow

### Step 1: Search
- Search arXiv, Semantic Scholar, Google Scholar
- Focus on papers from last 2 years
- De-duplicate across sources

### Step 2: Analyze Each Paper
For each relevant paper, extract:
- **Problem**: What gap does it address?
- **Method**: Core technical contribution (1-2 sentences)
- **Results**: Key numbers/claims
- **Relevance**: How does it relate to our work?

### Step 3: Synthesize
- Group papers by approach/theme
- Identify consensus vs disagreements
- Find gaps that our work could fill

### Step 4: Output
Present as a structured literature table:

```
| Paper | Venue | Method | Key Result | Relevance |
|-------|-------|--------|------------|-----------|
```

## Key Rules

- Always include paper citations (authors, year, venue)
- Distinguish between peer-reviewed and preprints
- Be honest about limitations of each paper
- Note if a paper directly competes with or supports our approach
