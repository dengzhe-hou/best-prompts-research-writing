# Best Prompts Research Writing

[中文](README.md) | 🇺🇸 English

Prompts and skills for research writing, each with its source stated. Pick whichever fits how you work:

- **Prompts**: 24 scenarios, each with a primary and an alternative candidate. Paste them into any chat model. Most prompt texts are in Chinese. [Open the prompt catalog](CATALOG_EN.md)
- **Skills**: 8 installable agent skills for Claude Code, Codex, or Cursor, suited to multi-step work. [Open the skill catalog](SKILLS_EN.md)

## Prompt or Skill?

| Your situation | Suggestion |
|---|---|
| You chat in ChatGPT, Claude, Kimi, or a similar web or mobile app | Use a prompt |
| Single-step task: translation, polishing, shortening or expanding, figure and table captions | A prompt is enough |
| Multi-step work in Claude Code, Codex, or Cursor: literature review, drafting a whole paper, rebuttal | Use a skill |
| You want to adapt it to your field or habits | Both are plain text; copy and edit. For a skill, edit its `SKILL.md` |

## What the Prompts Cover

| Category | Scenarios |
|---|---|
| [Translation](CATALOG_EN.md#i-translation) | Chinese to English, English to Chinese, Chinese rewriting |
| [Polishing](CATALOG_EN.md#ii-polishing) | English and Chinese polishing, de-AI editing |
| [Restructuring](CATALOG_EN.md#iii-restructuring) | Shortening, expansion, logic checks |
| [Paper sections](CATALOG_EN.md#iv-paper-sections) | Brainstorming, abstract, literature review, methods, results, conclusion, future work |
| [Experiments and figures](CATALOG_EN.md#v-experiments--figures) | Experiment analysis, figure selection, captions, architecture diagrams |
| [Review](CATALOG_EN.md#vi-review) | Reviewer-perspective review and responses to reviewers |

## What the Skills Cover

| Stage | Skills |
|---|---|
| Research | `idea-discovery` idea discovery · `research-lit` literature review · `research-gap` research gaps |
| Writing | `paper-writing` paper writing · `humanizer` English de-AI editing · `humanizer-zh-academic` Chinese de-AI editing |
| Review | `paper-review` paper review · `rebuttal` rebuttal |

Installation, sources, and links to the full upstream versions are in the [skill catalog](SKILLS_EN.md). These skills used to live in a separate best-skills-research-writing repository and have moved here.

## How Prompt Candidates Are Selected

Each scenario contains two candidates:

- **Primary candidate**: better aligned with the scenario's common inputs, outputs, and constraints.
- **Alternative candidate**: shorter, more specialized, or based on a different workflow.

Candidate order is an editorial judgment based on task fit, output clarity, and source traceability. It is not a model benchmark result. Prompt behavior varies by model, context, and field; users should verify facts, citations, data, and formatting.

## Prompt Sources and Usage Boundaries

Of the 48 prompt candidates, 41 are taken or adapted from these public projects and 7 were written for this catalog:

| Source | Entries | Main contributions | Upstream license |
|---|---|---|---|
| [Leey21/awesome-ai-research-writing](https://github.com/Leey21/awesome-ai-research-writing) | 16 | Primary candidates for translation, polishing, restructuring, experiments, figures, review | None stated |
| [ahmetbersoz/chatgpt-prompts-for-academic-writing](https://github.com/ahmetbersoz/chatgpt-prompts-for-academic-writing) | 10 | Brainstorming and paper sections; alternatives for English polishing, shortening, expansion | None stated |
| [alfonso0512/research-writing-skill](https://github.com/alfonso0512/research-writing-skill) | 13 | Alternative candidates across scenarios | [MIT](https://github.com/alfonso0512/research-writing-skill/blob/main/LICENSE), Copyright (c) 2026 research-writing-skill contributors |
| [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) | 1 | Responses to reviewers | [CC BY-NC 4.0](https://github.com/Imbad0202/academic-research-skills/blob/main/LICENSE) |
| [ChenLiu-1996/figures4papers](https://github.com/ChenLiu-1996/figures4papers) | 1 | Scientific figure references (described, text not reproduced) | [CC BY-NC 4.0](https://github.com/ChenLiu-1996/figures4papers/blob/main/LICENSE) |

Each candidate states its provenance: verbatim, adapted (with the upstream section named), or written for this catalog. Upstream licenses and usage terms vary; check the linked upstream repository before redistributing, modifying, or republishing its material. This catalog does not relicense third-party content.

Sources, adaptation notes, and licenses for the skills are in the [skill catalog](SKILLS_EN.md).

## Contributing

Contributions may add a new scenario, replace an existing candidate, or suggest a skill. A PR should include the prompt or skill text, source and usage terms, and at least one input/output example that demonstrates the practical difference. See the [PR template](.github/PULL_REQUEST_TEMPLATE.md) for the expected format.

Last reviewed: 2026-09-30
