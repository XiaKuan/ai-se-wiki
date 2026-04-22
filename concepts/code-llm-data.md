---
title: Code LLM Data Engineering (Code LLM数据工程与训练优化)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [code-llm-data, CCF-A, LLM, fine-tuning, research-trend]
sources: [ASE-2024]
---

## 定义

Code LLM数据工程与训练优化研究如何构建高质量的代码训练数据，以及如何针对软件工程任务微调大语言模型。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| DataRecipe — How to Cook the Data for CodeLLM? | ASE 2024 | **CodeLLM训练数据配方** |
| What Makes a High-Quality Training Dataset for LLMs: Practitioners' Perspective | ASE 2024 | 高质量数据集实践视角 |
| Maltracker: NPM Malware Tracker Copiloted by LLM-Enhanced Dataset | ISSTA 2024 | 恶意软件数据增强 |

### 关键技术

1. **Data Curation**: 数据选择、去噪、平衡
2. **Domain Adaptation**: 针对特定领域（安全、测试等）调整
3. **Synthetic Data Generation**: 利用LLM生成合成训练数据

## 核心问题

- 如何构建高质量代码训练数据？
- 数据选择、去噪、平衡策略？
- 代码数据的版权和许可问题？

## 相关方向

- [[test-generation]] — 测试生成可用于数据增强
- [[vibe-coding]] — Vibe Coding依赖高质量Code LLM
- [[program-comprehension]] — 程序理解模型的训练数据
