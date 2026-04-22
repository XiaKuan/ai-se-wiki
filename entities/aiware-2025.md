---
title: AIware 2025
created: 2026-04-23
updated: 2026-04-23
type: entity
tags: [aiware, ASE-2025, CCF-A, conference, AI-powered-Software, benchmark, dataset, multi-agent, aiops]
sources: [aiware-2025-program]
---

## 概述

**AIware 2025** 是与 ASE 2025（IEEE/ACM Automated Software Engineering）联合举办的学术会议，专注于 **AI-powered Software** 研究领域。AIware 2025 于 2025 年 11 月在韩国首尔（与 ASE 2025 同期）举行。

**官网**: https://2025.aiwareconf.org/
**Program**: https://2025.aiwareconf.org/program/program-aiware-2025/

## 会议特点

AIware 的定位是 **AI + Software Engineering 的交叉会议**，特别关注：
- LLM Agent 系统
- AI Agent 评估与基准
- 软件开发中的 AI 应用
- AI for SE（用 AI 辅助软件工程）

**重要 track**: AIware 设有 **Benchmark & Dataset Track**，专门发布运维/测试相关的数据集和评测基准，与 AI-Ops 研究直接相关。

## 与 CCF-A 的关系

AIware 不是 CCF-A 列表中的会议，但：
1. 与 ASE 2025 同期举办，共享部分设施
2. 论文质量较高，很多作者来自 CCF-A 会议
3. Benchmark & Dataset Track 对 AI-Ops 调研有重要参考价值

## Main Track 核心论文

| 论文 | 关键词 | 备注 |
|------|--------|------|
| **CHASE: LLM Agents for Dissecting Malicious PyPI Packages** | LLM Agent 安全 | 恶意包分析 |
| **Claude Code: From Single Agent in Terminal to Multi-Agent Systems** | Multi-Agent | Claude Code 架构演进 |
| **Demystifying LLM-based Software Engineering Agents** | SE Agent | 系统性分析 |
| **Automatically Maintaining Agent Systems: How Far Are We?** | Agent 维护 | 重要研究方向 |
| **Teaching LLMs to Debug: Toward Reasoning- and Tool-Aware Coding Agents** | 调试 Agent | 推理+工具感知 |
| **Ambient, Safe Agentic Automation on GitHub Platform** | 平台自动化 | GitHub Agent |
| **Judge the Votes: A System to Classify Bug Reports and Give Suggestions** | Bug 分类 | 运维辅助 |
| **Gemini CLI: The Terminal Renaissance** | CLI Agent | 多 Agent 终端 |

## Benchmark & Dataset Track 论文

| 论文 | 关键词 | 备注 |
|------|--------|------|
| **HPCAgentTester: A Multi-Agent LLM Approach for Enhanced HPC Unit Test Generation** | Multi-Agent 测试 | HPC 场景 |
| **SIR-Bench: Evaluating Investigation Depth in Security Incident Response Agents** | 事件响应评测 | 安全 Agent 评测 |
| **AutoBnB-RAG: Enhancing Multi-Agent Incident Response with RAG** | 事件响应 RAG | 多 Agent |
| **Understanding LLM-Driven Test Oracle Generation** | 测试预言生成 | 测试数据 |
| **Understanding the Characteristics of LLM-Generated Property-Based Tests** | 属性测试生成 | 测试质量 |
| **Turning Manual Tasks into Actions: Assessing Gemini-generated Selenium Tests** | Selenium 自动化 | 运维自动化 |

## 相关方向

- [[aiops-log-analysis]] — AIware 是 AI-Ops 研究的重要来源
- [[multi-agent-collaboration]] — Multi-Agent 是 AIware 的核心主题
- [[ASE-2025]] — AIware 与 ASE 2025 同期举办
- [[program-repair]] — Bug 修复是运维的重要组成部分
