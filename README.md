# Best Prompts Research Writing

🇨🇳 中文 | [English](README_EN.md)

科研写作用的 Prompt 和 Skill 合集，两者都逐条标明来源，按需自选：

- **Prompt**：24 个场景，每个场景一个首选候选和一个替代候选，复制到任何聊天模型里就能用。[打开 Prompt 目录](CATALOG.md)
- **Skill**：8 个可安装的 agent skill，装进 Claude Code、Codex 或 Cursor，适合多步流程。[打开 Skill 目录](SKILLS.md)

## Prompt 还是 Skill

| 你的情况 | 建议 |
|---|---|
| 在 ChatGPT、Claude、Kimi 等网页或 App 里对话 | 用 Prompt |
| 单步任务：翻译、润色、缩写扩写、写图表标题 | 用 Prompt 就够 |
| 在 Claude Code、Codex 或 Cursor 里做多步流程：文献综述、写整篇论文、审稿回复 | 用 Skill |
| 想按自己的领域和习惯调整 | 两者都是纯文本，复制后直接改；Skill 改的是 `SKILL.md` |

## Prompt 覆盖的任务

| 类别 | 场景 |
|---|---|
| [翻译](CATALOG.md#一翻译类-translation) | 中译英、英译中、中文重写 |
| [润色](CATALOG.md#二润色类-polishing) | 中英文润色、去 AI 味 |
| [结构调整](CATALOG.md#三结构调整类-restructuring) | 缩写、扩写、逻辑检查 |
| [论文段落](CATALOG.md#四论文各-section-生成-paper-sections) | 选题、摘要、综述、方法、结果、结论、未来工作 |
| [实验与图表](CATALOG.md#五实验与图表-experiments--figures) | 实验分析、绘图选择、图表标题、架构图 |
| [审稿](CATALOG.md#六审稿-review) | Reviewer 视角审阅、回复审稿人 |

## Skill 覆盖的流程

| 阶段 | Skill |
|---|---|
| 研究 | `idea-discovery` 想法发现 · `research-lit` 文献综述 · `research-gap` 研究空白 |
| 写作 | `paper-writing` 论文写作 · `humanizer` 英文去 AI 味 · `humanizer-zh-academic` 中文去 AI 味 |
| 审稿 | `paper-review` 论文审阅 · `rebuttal` 审稿回复 |

安装方法、各 skill 的来源和完整版链接见 [Skill 目录](SKILLS.md)。这些 skill 原先在单独的 best-skills-research-writing 仓库，现已并入本仓库。

## Prompt 候选的选择方式

每个场景包含两个候选：

- **首选候选**：更贴合该场景的常见输入、输出和约束。
- **替代候选**：更短、更专门，或采用不同工作方式。

候选顺序是维护者结合任务适配度、输出清晰度和来源可追溯性作出的编辑判断，不是模型基准测试结果。Prompt 效果会随模型、上下文和领域变化，使用者应检查事实、引用、数据和格式。

## Prompt 来源与使用边界

48 条 Prompt 候选中，41 条整理或改编自以下公开项目，7 条为本仓库编写：

| 来源 | 条数 | 主要贡献场景 | 上游许可 |
|---|---|---|---|
| [Leey21/awesome-ai-research-writing](https://github.com/Leey21/awesome-ai-research-writing) | 16 | 翻译、润色、结构调整、实验、图表、审稿的首选候选 | 仓库未声明 |
| [ahmetbersoz/chatgpt-prompts-for-academic-writing](https://github.com/ahmetbersoz/chatgpt-prompts-for-academic-writing) | 10 | 选题及论文各章节；英文润色、缩写、扩写的替代候选 | 仓库未声明 |
| [alfonso0512/research-writing-skill](https://github.com/alfonso0512/research-writing-skill) | 13 | 多场景替代候选 | [MIT](https://github.com/alfonso0512/research-writing-skill/blob/main/LICENSE)，Copyright (c) 2026 research-writing-skill contributors |
| [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) | 1 | 回复审稿人 | [CC BY-NC 4.0](https://github.com/Imbad0202/academic-research-skills/blob/main/LICENSE) |
| [ChenLiu-1996/figures4papers](https://github.com/ChenLiu-1996/figures4papers) | 1 | 科研绘图参考（只做介绍，未收录原文） | [CC BY-NC 4.0](https://github.com/ChenLiu-1996/figures4papers/blob/main/LICENSE) |

每条候选都注明来源类型：原文、改编（注明出自上游哪一部分），或本仓库编写。上游项目的许可证和使用条款各不相同；转载、修改或再发布前请检查对应上游仓库。本目录不替第三方内容重新授权。

Skill 的来源、改编方式和许可见 [Skill 目录](SKILLS.md)。

## 贡献

欢迎补充新场景、替换现有候选或推荐新的 skill。提交 PR 时请提供 Prompt 或 Skill 原文、来源与使用条款，以及至少一个能体现实际差异的输入输出示例。详细格式见 [PR 模板](.github/PULL_REQUEST_TEMPLATE.md)。

最后审阅：2026-09-30
