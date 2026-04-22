---
title: Code Review & Static Analysis (LLM辅助代码审查与静态分析)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [code-review, CCF-A, LLM, static-analysis, research-trend]
sources: [ASE-2024, ISSTA-2024]
---

## 定义

LLM辅助代码审查与静态分析研究如何利用大语言模型辅助或自动化代码审查过程，以及结合静态分析工具提升效果。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation | ASE 2024 | 多Agent代码审查推荐 |
| iSMELL: Assembling LLMs with Expert Toolsets for Code Smell Detection | ASE 2024 | 代码气味检测工具集成 |
| Large Language Models Can Connect the Dots: Model Optimization Bugs | ISSTA 2024 | 深度学习模型优化bug发现 |
| An Empirical Study of Static Analysis Tools for Secure Code Review | ISSTA 2024 | 安全代码审查静态工具实证 |

## 核心问题

- LLM能否替代人工代码审查？
- 如何让LLM结合静态分析工具？
- 代码审查的一致性和可扩展性？

## 相关方向

- [[multi-agent-collaboration]] — 代码审查可由多Agent协作完成
- [[llm-security]] — 安全代码审查是重要子方向
- [[code-quality-assessment]] — 代码审查本质是质量评估
