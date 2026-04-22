---
title: Test Generation (LLM驱动的自动化测试生成)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [test-generation, CCF-A, LLM, benchmark, research-trend]
sources: [ASE-2024, ISSTA-2024]
---

## 定义

LLM驱动的自动化测试生成指利用大语言模型自动生成测试用例、测试输入、测试驱动代码的技术方向。这是目前SE领域最热门的研究方向之一，在CCF-A会议中论文数量最多。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| SlicePromptTest4J: High-coverage Test Generation using LLM via Method Slicing | ASE 2024 | 通过方法切片提升LLM测试覆盖率 |
| LLM4Fin: Fully Automating LLM-Powered Test Case Generation for FinTech | ISSTA 2024 | 金融软件测试用例自动生成 |
| Towards Understanding the Effectiveness of LLM on Directed Test Input Generation ⭐ | ASE 2024 | **Distinguished Paper** - 理解LLM测试生成有效性 |
| UniTSyn: Large-Scale Dataset for Enhancing LLM for Program Testing | ISSTA 2024 | **基准数据集** |
| Domain Adaptation for Code Model-Based Unit Test Case Generation | ISSTA 2024 | 领域自适应测试生成 |
| How Effective Are They? Exploring LLM Based Fuzz Driver Generation | ISSTA 2024 | Fuzz驱动生成 |

### 关键技术

1. **Method Slicing (方法切片)**: 将目标方法按依赖关系切片，帮助LLM更好地理解上下文
2. **Domain Adaptation (领域自适应)**: 针对特定领域（金融、区块链等）调整测试生成策略
3. **Fuzz Driver Generation**: 生成模糊测试驱动代码
4. **Oracle Guidance**: Oracle引导的程序选择

## 核心问题

- 如何让LLM生成高覆盖率、低冗余、可执行的测试用例？
- 如何处理测试预言(Oracle)的自动生成？
- 如何评估LLM生成测试的质量？

## 相关方向

- [[program-repair]] — 测试生成常与程序修复结合
- [[code-quality-assessment]] — 测试质量评估是相关问题
- [[vibe-coding]] — Vibe Coding依赖高质量测试验证生成代码
