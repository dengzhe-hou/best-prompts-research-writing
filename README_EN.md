# Best Prompts Research Writing

[中文](README.md) | 🇺🇸 English

A prompt catalog for focused research-writing tasks: 24 scenarios, each with a primary candidate and a meaningfully different alternative, with traceable sources and copy-ready text.

[Open the English prompt catalog](CATALOG_EN.md)

## What It Covers

| Category | Scenarios |
|---|---|
| [Translation](CATALOG_EN.md#i-translation) | Chinese to English, English to Chinese, Chinese rewriting |
| [Polishing](CATALOG_EN.md#ii-polishing) | English and Chinese polishing, de-AI editing |
| [Restructuring](CATALOG_EN.md#iii-restructuring) | Shortening, expansion, logic checks |
| [Paper sections](CATALOG_EN.md#iv-paper-sections) | Brainstorming, abstract, literature review, methods, results, conclusion, future work |
| [Experiments and figures](CATALOG_EN.md#v-experiments--figures) | Experiment analysis, figure selection, captions, architecture diagrams |
| [Review](CATALOG_EN.md#vi-review) | Reviewer-perspective review and responses to reviewers |

## Relationship to Best Skills

This repository provides prompts for focused, single-session tasks.

[best-skills-research-writing](https://github.com/dengzhe-hou/best-skills-research-writing) provides installable agent skills for multi-step literature research, paper writing, review, and rebuttal workflows. The two repositories complement rather than replace each other.

## How Candidates Are Selected

Each scenario contains two candidates:

- **Primary candidate**: better aligned with the scenario's common inputs, outputs, and constraints.
- **Alternative candidate**: shorter, more specialized, or based on a different workflow.

Candidate order is an editorial judgment based on task fit, output clarity, and source traceability. It is not a model benchmark result. Prompt behavior varies by model, context, and field; users should verify facts, citations, data, and formatting.

## Sources and Usage Boundaries

Of the 48 candidates, 41 are taken or adapted from these public projects and 7 were written for this catalog:

| Source | Entries | Main contributions | Upstream license |
|---|---|---|---|
| [Leey21/awesome-ai-research-writing](https://github.com/Leey21/awesome-ai-research-writing) | 16 | Primary candidates for translation, polishing, restructuring, experiments, figures, review | None stated |
| [ahmetbersoz/chatgpt-prompts-for-academic-writing](https://github.com/ahmetbersoz/chatgpt-prompts-for-academic-writing) | 10 | Brainstorming and paper sections; alternatives for English polishing, shortening, expansion | None stated |
| [alfonso0512/research-writing-skill](https://github.com/alfonso0512/research-writing-skill) | 13 | Alternative candidates across scenarios | [MIT](https://github.com/alfonso0512/research-writing-skill/blob/main/LICENSE), Copyright (c) 2026 research-writing-skill contributors |
| [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) | 1 | Responses to reviewers | [CC BY-NC 4.0](https://github.com/Imbad0202/academic-research-skills/blob/main/LICENSE) |
| [ChenLiu-1996/figures4papers](https://github.com/ChenLiu-1996/figures4papers) | 1 | Scientific figure references (described, text not reproduced) | [CC BY-NC 4.0](https://github.com/ChenLiu-1996/figures4papers/blob/main/LICENSE) |

Each candidate states its provenance: verbatim, adapted (with the upstream section named), or written for this catalog. Upstream licenses and usage terms vary; check the linked upstream repository before redistributing, modifying, or republishing its material. This catalog does not relicense third-party content.

## Contributing

Contributions may add a new scenario or replace an existing candidate. A PR should include the prompt text, source and usage terms, and at least one input/output example that demonstrates the practical difference. See the [PR template](.github/PULL_REQUEST_TEMPLATE.md) for the expected format.

Last reviewed: 2026-09-30
