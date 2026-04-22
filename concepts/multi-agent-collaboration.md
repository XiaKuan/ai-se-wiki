---
title: Multi-Agent Collaboration (多LLM Agent协作系统)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [multi-agent, CCF-A, LLM, workflow-automation, research-trend]
sources: [ASE-2024]
---

## 定义

多LLM Agent协作系统指多个大语言模型Agent协同工作，共同完成复杂软件工程任务的系统范式。这是2024年新爆发的研究方向，代表了从"LLM as Tool"到"LLM as Collaborator"的范式转变。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation | ASE 2024 | **多Agent协作代码审查** |
| Prompt Sapper: LLM-Empowered Production Tool for Building AI Chains | ASE 2024 | **AI Chain构建工具** |
| CoqPilot: LLM-based generation of Coq proofs | ASE 2024 | Agent辅助形式化证明 |
| Can Cooperative Multi-Agent Reinforcement Learning Boost Automatic Web Testing? | ASE 2024 | 多Agent强化学习网页测试 |

### 协作模式

1. **分工协作模式**: 不同Agent负责不同子任务（如一个负责代码生成，一个负责测试验证）
2. **串行Chain模式**: Agent形成处理链，上一个Agent输出作为下一个输入
3. **并行投票模式**: 多个Agent独立处理，投票决定最终结果

## 核心问题

- 多个LLM Agent如何有效分工？
- 如何保证多Agent协作的一致性和可解释性？
- Agent之间的通信协议如何设计？
- 如何处理Agent协作中的错误传播？

## 相关方向

- [[workflow-automation]] — AI Chain是工作流自动化的具体实现
- [[code-review-static-analysis]] — 代码审查是多Agent协作的典型场景
- [[program-repair]] — 多Agent可用于程序修复的不同阶段
