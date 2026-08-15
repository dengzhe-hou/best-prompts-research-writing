# Best Prompts Research Writing

🇨🇳 中文 | [English](README_EN.md)

面向科研写作单项任务的 Prompt 目录：24 个场景，每个场景提供一个首选候选和一个替代候选，保留来源说明，可直接复制使用。

[打开中文 Prompt 目录](CATALOG.md)

## 适合什么任务

| 类别 | 场景 |
|---|---|
| [翻译](CATALOG.md#一翻译类-translation) | 中译英、英译中、中文重写 |
| [润色](CATALOG.md#二润色类-polishing) | 中英文润色、去 AI 味 |
| [结构调整](CATALOG.md#三结构调整类-restructuring) | 缩写、扩写、逻辑检查 |
| [论文段落](CATALOG.md#四论文各-section-生成-paper-sections) | 选题、摘要、综述、方法、结果、结论、未来工作 |
| [实验与图表](CATALOG.md#五实验与图表-experiments--figures) | 实验分析、绘图选择、图表标题、架构图 |
| [审稿](CATALOG.md#六审稿-review) | Reviewer 视角审阅、回复审稿人 |

## 和 Best Skills 的区别

这个仓库提供可以单次复制使用的 Prompt，适合边界明确的单项任务。

[best-skills-research-writing](https://github.com/dengzhe-hou/best-skills-research-writing) 提供可安装的 agent skills，适合文献研究、论文写作和审稿回复等多步骤工作流。两者互补，不互相替代。

## 选择方式

每个场景包含两个候选：

- **首选候选**：更贴合该场景的常见输入、输出和约束。
- **替代候选**：更短、更专门，或采用不同工作方式。

候选顺序是维护者结合任务适配度、输出清晰度和来源可追溯性作出的编辑判断，不是模型基准测试结果。Prompt 效果会随模型、上下文和领域变化，使用者应检查事实、引用、数据和格式。

## 来源与使用边界

本目录整理并改编自以下公开项目：

| 来源 | 主要贡献场景 |
|---|---|
| [Leey21/awesome-ai-research-writing](https://github.com/Leey21/awesome-ai-research-writing) | 翻译、润色、结构调整、实验、图表、审稿 |
| [ahmetbersoz/chatgpt-prompts-for-academic-writing](https://github.com/ahmetbersoz/chatgpt-prompts-for-academic-writing) | 选题及论文各章节 |
| [alfonso0512/research-writing-skill](https://github.com/alfonso0512/research-writing-skill) | 多场景替代候选 |
| [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) | 文献综述、审稿、回复审稿人 |
| [kaixindelele/ChatPaper](https://github.com/kaixindelele/ChatPaper) | 审稿候选 |
| [ChenLiu-1996/figures4papers](https://github.com/ChenLiu-1996/figures4papers) | 科研绘图参考 |

Prompt 条目保留对应来源链接。上游项目的许可证和使用条款各不相同，部分项目没有 GitHub 可识别的 SPDX 许可证；转载、修改或再发布前请检查对应上游仓库。本目录不替第三方内容重新授权。

## 贡献

欢迎补充新场景或替换现有候选。提交 PR 时请提供 Prompt 原文、来源与使用条款，以及至少一个能体现实际差异的输入输出示例。详细格式见 [PR 模板](.github/PULL_REQUEST_TEMPLATE.md)。

最后审阅：2026-08-15
