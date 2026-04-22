---
title: Vibe Coding (自然语言代码生成与Vibe Coding)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [vibe-coding, CCF-A, LLM, research-trend]
sources: [ASE-2024, arXiv]
---

## 定义

Vibe Coding指用户通过自然语言描述需求，由AI系统自动生成完整代码的新型软件开发范式。用户关注"做什么"而非"怎么做"，代码生成的质量评估是核心挑战。

## 研究现状

### 核心论文

| 论文 | 来源 | 亮点 |
|------|------|------|
| PlayCoder: Making LLM-Generated GUI Code Playable | ASE/arXiv | GUI代码可执行性 |
| CoEdPilot: Recommending Code Edits with Learned Prior Edit Relevance | ISSTA 2024 | 交互式代码编辑推荐 |
| Calico: Automated Knowledge Calibration for AI Mastery in Code Tasks | ISSTA 2024 | AI代码任务知识校准 |

## 核心问题

- 自然语言描述和生成代码之间的语义鸿沟？
- 如何评估"Vibe Coding"的代码质量？
- 开发者如何有效纠错和反馈？
- 生成代码的可维护性问题？

## 相关方向

- [[code-quality-assessment]] — Vibe Coding特别需要质量评估
- [[test-generation]] — 测试验证是质量保证的关键
- [[workflow-automation]] — Vibe Coding是工作流自动化的终极目标
