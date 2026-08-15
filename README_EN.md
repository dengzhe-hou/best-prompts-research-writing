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

The catalog curates and adapts material from these public projects:

| Source | Main contributions |
|---|---|
| [Leey21/awesome-ai-research-writing](https://github.com/Leey21/awesome-ai-research-writing) | Translation, polishing, restructuring, experiments, figures, review |
| [ahmetbersoz/chatgpt-prompts-for-academic-writing](https://github.com/ahmetbersoz/chatgpt-prompts-for-academic-writing) | Brainstorming and paper sections |
| [alfonso0512/research-writing-skill](https://github.com/alfonso0512/research-writing-skill) | Alternative candidates across scenarios |
| [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) | Literature review, paper review, responses to reviewers |
| [kaixindelele/ChatPaper](https://github.com/kaixindelele/ChatPaper) | Review candidates |
| [ChenLiu-1996/figures4papers](https://github.com/ChenLiu-1996/figures4papers) | Scientific figure references |

Each prompt entry retains its source link. Upstream licenses and usage terms vary, and some projects do not expose a GitHub-detected SPDX license. Check the linked upstream repository before redistributing, modifying, or republishing its material. This catalog does not relicense third-party content.

## Contributing

Contributions may add a new scenario or replace an existing candidate. A PR should include the prompt text, source and usage terms, and at least one input/output example that demonstrates the practical difference. See the [PR template](.github/PULL_REQUEST_TEMPLATE.md) for the expected format.

Last reviewed: 2026-08-15
