[项目首页](README.md) | 🇨🇳 中文 Skill 目录 | [English skill catalog](SKILLS_EN.md)

---

# Research Writing Skill Catalog

> 8 个可安装的 agent skill，覆盖研究、写作、审稿。每个场景一个首选候选（收录在本仓库 `skills/` 下），部分场景另有一个替代候选（只给链接）。

> 收录的 skill 大多是上游的精简版，篇幅约为 2026 年 5 月上游版本的 7% 到 22%。短、好读、装上就能用，但功能比原版少，有的还会调用本仓库没有收录的子 skill。每条都写明删掉了什么，并给出原版链接；需要完整功能请装原版。

---

## 安装

`idea-discovery`、`research-lit`、`paper-writing`、`rebuttal` 与 [ARIS](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) 原版同名，照下面的"全部安装"会覆盖原版。已经装了 ARIS 的，用第二条命令只装另外 4 个。

**Claude Code**

```bash
git clone https://github.com/dengzhe-hou/best-prompts-research-writing.git
mkdir -p ~/.claude/skills

# 全部安装
for d in best-prompts-research-writing/skills/*/; do cp -R "${d%/}" ~/.claude/skills/; done

# 已装 ARIS 原版的：只装不同名的 4 个
for n in research-gap paper-review humanizer humanizer-zh-academic; do cp -R best-prompts-research-writing/skills/$n ~/.claude/skills/; done

# 只装一个，例如 rebuttal
cp -R best-prompts-research-writing/skills/rebuttal ~/.claude/skills/
```

**Codex**：把上面的 `~/.claude/skills` 换成 `~/.codex/skills`。

**Cursor**：会读取 `~/.claude/skills/` 和 `~/.codex/skills/`，按上面任一种装好即可。

装好后，在 Claude Code 和 Cursor 里用 `/skill 名` 调用（例如 `/rebuttal`），在 Codex 里输入 `$rebuttal` 或用 `/skills` 从列表里选。也可以直接说要做的事。

---

## 📌 快速导航

| 阶段 | 场景 |
|---|---|
| 研究 | [1.1 想法发现](#11-想法发现) · [1.2 文献综述](#12-文献综述) · [1.3 研究空白](#13-研究空白) |
| 写作 | [2.1 论文写作](#21-论文写作) · [2.2 英文去 AI 味](#22-英文去-ai-味) · [2.3 中文去 AI 味](#23-中文去-ai-味) |
| 审稿 | [3.1 论文审阅](#31-论文审阅) · [3.2 审稿回复](#32-审稿回复) |

---

# 一、研究

## 1.1 想法发现

### 首选候选：`idea-discovery`

> 来源：精简自 [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/idea-discovery/SKILL.md)（MIT），约为上游 5 月版本的 16%

**做什么**：文献调研、生成想法、查新、评审四步，最后输出排好序的想法报告。

**注意**：会调用 `/idea-creator`、`/novelty-check`、`/research-review` 三个子 skill，本仓库没有收录。原版的跨模型审查、pilot 实验和检查点都已删去。

**文件**：[`skills/idea-discovery/SKILL.md`](skills/idea-discovery/SKILL.md)

### 替代候选（仅链接）

> [lishix520/academic-paper-skills](https://github.com/lishix520/academic-paper-skills)（MIT）

学术论文的规划与写作框架。

---

## 1.2 文献综述

### 首选候选：`research-lit`

> 来源：精简自 [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/research-lit/SKILL.md)（MIT），约为上游 5 月版本的 8%

**做什么**：在 arXiv、Semantic Scholar、Google Scholar 检索，去重、分析、综合，输出文献对比表。

**注意**：文件里列出的 Zotero、Obsidian、DeepXiv、Exa、Gemini、OpenAlex 需要原版附带的脚本或 MCP 服务，本仓库没有。原版的 Research Wiki 已删去。

**文件**：[`skills/research-lit/SKILL.md`](skills/research-lit/SKILL.md)

### 替代候选（仅链接）

> [Weizhena/Deep-Research-skills](https://github.com/Weizhena/Deep-Research-skills)（MIT）

结构化深度研究，分大纲、研究、报告三步，中间有人工确认。

---

## 1.3 研究空白

### 首选候选：`research-gap`

> 来源：本仓库编写，没有对应的上游 skill

**做什么**：按方法、理论、实证、应用四类找研究空白，评估重要性和可行性，输出结构化报告。

**文件**：[`skills/research-gap/SKILL.md`](skills/research-gap/SKILL.md)

### 替代候选（仅链接）

> [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills)（CC BY-NC 4.0）

研究、写作、审稿、修订、定稿全流程。

---

# 二、写作

## 2.1 论文写作

### 首选候选：`paper-writing`

> 来源：精简自 [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/paper-writing/SKILL.md)（MIT），约为上游 5 月版本的 7%

**做什么**：列出规划、作图、写 LaTeX、编译、改进循环五个阶段。

**注意**：这个精简版更像流程提纲。每个阶段都要调用子 skill（`/paper-plan`、`/paper-figure`、`/paper-write`、`/paper-compile`、`/auto-paper-improvement-loop`），本仓库都没有；原版的跨模型审查和 assurance gate 也已删去。实际写论文请装原版。

**文件**：[`skills/paper-writing/SKILL.md`](skills/paper-writing/SKILL.md)

### 替代候选（仅链接）

> [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills)（MIT）

面向 ML、CV、NLP 论文，改编自彭思达教授的公开笔记。

---

## 2.2 英文去 AI 味

### 首选候选：`humanizer`

> 来源：精简自 [blader/humanizer](https://github.com/blader/humanizer/blob/main/SKILL.md)（MIT），约为上游 5 月版本的 10%

**做什么**：按 Wikipedia 的 "Signs of AI writing" 识别 11 类 AI 写作痕迹（上游 5 月版本有 29 类），改写后再自查一遍残留痕迹。

**注意**：每类后面一行的 Fix 建议是本仓库加的。

**文件**：[`skills/humanizer/SKILL.md`](skills/humanizer/SKILL.md)

### 替代候选（仅链接）

> [matsuikentaro1/humanizer_academic](https://github.com/matsuikentaro1/humanizer_academic)（MIT）

基于 humanizer，面向医学论文。

---

## 2.3 中文去 AI 味

### 首选候选：`humanizer-zh-academic`

> 来源：精简自 [redbaronyyyyy-eng/humanizer-zh-academic](https://github.com/redbaronyyyyy-eng/humanizer-zh-academic/blob/main/SKILL.md)（MIT），约为上游的 22%

**做什么**：识别 6 种中文学术写作的 AI 腔（上游有 16 种），按固定流程改写并自评。上游的目标是降低 AIGC 检测率，本仓库没有验证过效果。

**文件**：[`skills/humanizer-zh-academic/SKILL.md`](skills/humanizer-zh-academic/SKILL.md)

---

# 三、审稿

## 3.1 论文审阅

### 首选候选：`paper-review`

> 来源：改写自 [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/research-review/SKILL.md) 的 research-review 和 idea-discovery 的外部评审部分（MIT）；评审维度和输出模板为本仓库增补

**做什么**：从新颖性、重要性、可行性、实验设计、写作质量五个维度评审，按严重程度列问题，给 1 到 10 分。

**注意**：文件里写了 cross-model review，但没有接入第二个模型，实际由当前模型扮演审稿人，只评一轮。

**文件**：[`skills/paper-review/SKILL.md`](skills/paper-review/SKILL.md)

### 替代候选（仅链接）

> [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills)（CC BY-NC 4.0）

包含审稿与修订流程。

---

## 3.2 审稿回复

### 首选候选：`rebuttal`

> 来源：精简自 [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/skills/rebuttal/SKILL.md)（MIT），约为上游 5 月版本的 14%

**做什么**：拆解审稿意见，制定回复策略，按字数上限起草。有三道安全门：每条事实要有出处；每个承诺要么已经做到，要么经你批准，要么只写成未来工作；每条意见都要有交代。不许编造数据和引用。

**注意**：原版的外部审稿模型、进度文件和命令行参数已删去。第 6 步写的 External reviewer 由当前模型扮演，不接入第二个模型。用的时候在对话里直接说明会议名称和字数上限。

**文件**：[`skills/rebuttal/SKILL.md`](skills/rebuttal/SKILL.md)

---

# 来源与许可

| 上游 | 许可 | 本仓库收录 |
|---|---|---|
| [wanshuiyin/Auto-claude-code-research-in-sleep](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep) | [MIT](https://github.com/wanshuiyin/Auto-claude-code-research-in-sleep/blob/main/LICENSE)，Copyright (c) 2026 wanshuiyin | `idea-discovery`、`research-lit`、`paper-writing`、`paper-review`、`rebuttal` |
| [blader/humanizer](https://github.com/blader/humanizer) | [MIT](https://github.com/blader/humanizer/blob/main/LICENSE)，Copyright (c) 2025 Siqi Chen | `humanizer` |
| [redbaronyyyyy-eng/humanizer-zh-academic](https://github.com/redbaronyyyyy-eng/humanizer-zh-academic) | [MIT](https://github.com/redbaronyyyyy-eng/humanizer-zh-academic/blob/main/LICENSE)，Copyright (c) 2025 redbaronyyyyy-eng | `humanizer-zh-academic` |

本仓库对这些 skill 的精简和改写以 MIT 发布，见 [`skills/LICENSE`](skills/LICENSE)。替代候选只给链接，不复制内容。

# 贡献 skill

欢迎推荐新 skill。请注明来源仓库、许可，以及是原文、精简还是原创。只有 MIT 或兼容许可的 skill 才复制进本仓库，其余只放链接。

最后审阅：2026-09-30
