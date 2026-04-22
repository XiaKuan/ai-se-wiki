---
title: Program Comprehension (LLM程序理解与代码摘要)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [program-comprehension, CCF-A, LLM, research-trend]
sources: [ISSTA-2024, ASE-2024]
---

## 定义

LLM程序理解与代码摘要研究如何利用大语言模型理解代码语义、生成代码摘要、解释代码功能，帮助开发者理解复杂代码库。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| NativeSummary: Summarizing Native Binary Code for Android Static Analysis | ISSTA 2024 | 二进制代码摘要 |
| SelfPiCo: Self-Guided Partial Code Execution with LLMs | ISSTA 2024 | 部分代码执行理解 |
| LPR: Large Language Models-Aided Program Reduction | ISSTA 2024 | 程序归约辅助 |

## 核心问题

- LLM能否理解复杂代码库的语义？
- 二进制/汇编级别的代码理解？
- 跨语言代码理解可行性？
- 代码摘要的质量和一致性？

## 相关方向

- [[code-quality-assessment]] — 代码理解是质量评估的基础
- [[formal-verification]] — 程序理解支撑形式化验证
- [[aiops-log-analysis]] — 日志理解依赖程序理解能力
