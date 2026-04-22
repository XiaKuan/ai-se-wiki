---
title: Code Quality Assessment (LLM代码生成质量评估)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [code-quality-assessment, CCF-A, LLM, evaluation, research-trend]
sources: [ASE-2024, ISSTA-2024]
---

## 定义

LLM代码生成质量评估研究如何系统性地评估大语言模型生成代码的正确性、可读性、效率、安全性等质量维度。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| PlayCoder: Making LLM-Generated GUI Code Playable | ASE 2024 | GUI代码可执行性评估 |
| When to Stop? Towards Efficient Code Generation with Excess Token Prevention | ISSTA 2024 | 生成效率与质量平衡 |
| Oracle-Guided Program Selection from Large Language Models | ISSTA 2024 | Oracle引导的程序选择 |
| Towards Understanding the Effectiveness of LLM on Directed Test Input Generation ⭐ | ASE 2024 | LLM测试生成有效性分析 |

### 评估维度

1. **语法正确性**: 生成代码能否编译/解释执行
2. **语义正确性**: 生成代码是否满足需求
3. **覆盖效率**: 测试用例对代码的覆盖程度
4. **可读性**: 代码可维护性和可理解性
5. **安全性**: 是否存在安全漏洞

## 核心问题

- 如何自动化评估LLM生成代码的质量？
- 何时停止生成以避免"幻觉"(Hallucination)？
- 如何在多轮对话中保持代码一致性？

## 相关方向

- [[test-generation]] — 测试生成常用于验证代码质量
- [[program-comprehension]] — 代码理解是质量评估的基础
- [[vibe-coding]] — Vibe Coding特别需要质量评估
