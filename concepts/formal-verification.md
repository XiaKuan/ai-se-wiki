---
title: Formal Verification (LLM辅助形式化验证与定理证明)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [formal-verification, CCF-A, LLM, research-trend]
sources: [ASE-2024]
---

## 定义

LLM辅助形式化验证与定理证明研究大语言模型在形式化方法中的应用，包括辅助定理证明、验证条件生成、保证案例分析等。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| CoqPilot: LLM-based generation of Coq proofs | ASE 2024 | 证明助手 |
| CoDefeater: Using LLMs To Find Defeaters in Assurance Cases | ASE 2024 | 保障案例中的LLM |
| On Reasoning-Centric LLM-based Automated Theorem Proving | arXiv | 推理中心定理证明 |

### 技术路线

1. **Proof Assistant Integration**: 与Coq、Isabelle等证明助手集成
2. **Verification Condition Generation**: 自动生成验证条件
3. **Defeater Discovery**: 发现保障案例中的反例

## 核心问题

- LLM能否理解并生成形式化证明？
- 如何将自然语言推理转化为符号推理？
- 形式化验证的"最后一公里"问题

## 相关方向

- [[program-comprehension]] — 程序理解是形式化验证的基础
- [[multi-agent-collaboration]] — CoqPilot展示了Agent协作在证明中的应用
- [[test-generation]] — 测试可视为轻量级验证
