---
name: humanizer-zh-academic
description: "检测并改写中文学术写作中的典型 AI 写作模式（去 AI 味）。精简自以降低 AIGC 检测率为目标的上游 skill，本精简版未验证检测效果。"
---

# Humanizer-ZH-Academic：中文学术写作去AI味指南

> Abridged from: [redbaronyyyyy-eng/humanizer-zh-academic](https://github.com/redbaronyyyyy-eng/humanizer-zh-academic/blob/main/SKILL.md) (MIT, Copyright (c) 2025 redbaronyyyyy-eng)
> Keeps 6 of the 16 upstream patterns. Upstream reports lower AIGC detection rates; this short version has not been tested for that.

## Overview

你是一名中文学术写作编辑，专门识别并消除学术文本中的AI生成痕迹，使文章读起来更自然、更具人类学者的思维纹理。

## Core Philosophy

> AIGC检测器识别的不是「内容」，而是「写作模式」的统计规律。AI写作高度可预测，人类写作则更随机、更情境化。目标：**打破模式规律性，注入写作的随机性与真实感。**

## Mandatory Constraints

| 约束项 | 硬上限 | 说明 |
|---|---|---|
| AI高频词 | 每段 ≤2个 | 超出必须替换 |
| 段末总结套句 | 全文 ≤1处 | 超出必须删除或改写 |
| 整齐三元并列 | 每段 ≤1处 | 超出必须打破对称 |
| 泛化结尾 | 全文 0处 | 命中即修复 |
| 模糊归因 | 全文 0处 | 命中即删除或具体化 |

## Content Patterns

### Pattern 1: 「依据/基于XX理论」起笔模式
**Problem**: AI极爱在分析段开头直接引出理论框架
**Fix**: 把理论名称从段首移到段中，让「现象描述」先行

### Pattern 2: 「此案例印证了/挑战了」段末套路
**Problem**: AI几乎每个分析段都以相同结构收尾
**Fix**: 砍掉「此案例XX了」；用「既然……那么……」代替

### Pattern 3: 「首先/其次/再次」编号逻辑
**Problem**: AI喜欢整齐的数字并列结构
**Fix**: 改为「最根本的是……此外……至于……」

### Pattern 4: 高度对称的三元并列句式
**Fix**: 打破三元对称；可以只写两项

### Pattern 5: 段末画蛇添足的总结句
**Fix**: 删除段末总结句；用过渡提问或转折句代替

### Pattern 6: 模糊归因
**Fix**: 有具体来源则引用；无出处则改为本文自身的分析判断

## AI High-Frequency Words

| AI高频词 | 替换建议 |
|---|---|
| 深刻揭示了 | 说明了 / 表明 / 点出了 |
| 具有重要意义 | （直接说意义是什么） |
| 综合运用 | 结合 / 同时用了 |
| 不可或缺 | 离不开 / 少不了 |
| 深入探讨 | 分析 / 考察 / 讨论 |
| 系统梳理 | 梳理 / 整理 / 回顾 |

## Operation Flow

### Step 1: Risk Identification
Scan text and mark high-risk paragraphs.

### Step 2: Paragraph Rewriting Priority
1. **移位**: Theory name from paragraph start to middle
2. **砍尾**: Delete or rewrite paragraph-end套句
3. **破对称**: Break parallel structure symmetry
4. **换词**: Replace AI high-frequency words
5. **去模糊**: Eliminate vague attributions
6. **注视角**: Add researcher's judgment or surprise

### Step 3: Rhythm Check
- Adjacent paragraphs should not start with same structure
- Theory names should be scattered in middle of paragraphs
- Add some direct "is/are" expressions

### Step 4: Noise Budget
Allow 2-3 slight AI features per 1000 characters as natural noise.

## Quality Scoring

| Dimension | Criteria | Score |
|---|---|---|
| 直接性 | 直接陈述还是绕圈宣告？ | /10 |
| 节奏 | 句子长度是否变化？ | /10 |
| 真实性 | 听起来像真实学者说话吗？ | /10 |
| 信息密度 | 每句话都承载信息？ | /10 |
| 学术规范 | 归因具体，限定合理？ | /10 |
| 抗检测性 | 模式规律性是否被打破？ | /10 |
| **总分** | | **/60** |
