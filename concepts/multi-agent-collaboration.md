---
title: Multi-Agent Collaboration (多LLM Agent协作系统)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [multi-agent, CCF-A, LLM, workflow-automation, research-trend, ASE-2024, ASE-2025, ICSE-2025, ICSE-2026, FSE-2024]
sources: [ASE-2024, ASE-2025, ICSE-2025, ICSE-2026, FSE-2024, arXiv]
---

## 定义

多LLM Agent协作系统指多个大语言模型Agent协同工作，共同完成复杂软件工程任务的系统范式。这是2024年新爆发的研究方向，代表了从"LLM as Tool"到"LLM as Collaborator"的范式转变。

## CCF-A会议调研结果（2026年4月更新）

### 核心发现

经过对 **ICSE 2024-2026、FSE 2024-2025、ASE 2025、ISSTA 2024、PLDI 2025、POPL 2025、OSDI 2025** 的逐一检查：

- **Multi-agent collaboration 在 CCF-A SE 会议中是一个非常新的方向**
- 2024年各 CCF-A 会议（ICSE/FSE/ASE/ISSTA）**几乎空白**
- 2025年开始出现零星 agent 论文，但数量极少
- **2026年 ICSE 是目前 multi-agent SE 论文最集中的 CCF-A 会议**

### CCF-A 会议逐个检查结果

| 会议 | Multi-Agent 相关论文 | 备注 |
|------|---------------------|------|
| **ICSE 2026** | 4篇确认 | 最多，包含SWE-Debate、Rust Agent、Agentic AI in OSS-Fuzz |
| **ICSE 2025** | 1篇确认（Human-In-the-Loop SD Agents）| SEIP track |
| **FSE 2024** | 0篇 | 无multi-agent直接命中 |
| **FSE 2025** | 未知 | 页面未上线或无相关论文 |
| **ASE 2025** | 多篇 | AgenticSE workshop + 主会 |
| **ISSTA 2024** | 0篇 | 之前已确认无 |
| **PLDI/POPL/OSDI** | 0篇 | 系统/PL会议，非SE主战场 |
| **SOSP/OOPSLA** | 未确认 | 网络超时 |

## ICSE 2026 确认论文（2026年4月，里约热内卢）

| 论文 | 关键词 | 备注 |
|------|--------|------|
| **SWE-Debate: Competitive Multi-Agent Debate for Software Issue Resolution** (arXiv:2511.08475) | 多Agent辩论 | Han Li等，上交 |
| **Unified Software Engineering Agent as AI Software Engineer** | 统一Agent | 完整SE流程 |
| **Unlocking LLM Repair Capabilities Through Cross-Language Translation and Multi-Agent Refinement** | 跨语言+多Agent | — |
| **Evaluating and Improving Automated Repository-Level Rust Issue Resolution with LLM-based Agents** | LLM-based Agents | Jiahong Xiang等，南科大 |
| **More with Less: An Empirical Study of Turn-Control Strategies for Efficient Coding Agents** | 高效编码Agent | — |
| **Fixing Security Vulnerabilities with Agentic AI in OSS-Fuzz** | Agentic AI安全修复 | Yuntong Zhang，NUS |

> 注：以上论文来自 ICSE 2026 官方页面 + DBLP/arXiv，需最终以官方发布为准。

## ICSE 2025 确认论文（2025年4月，渥太华）

| 论文 | Track | 亮点 |
|------|-------|------|
| **Human-In-the-Loop Software Development Agents** | SEIP | 开发者-Agent协作实证研究 |

## ASE 2025 确认论文（2025年11月，首尔）

| 论文 | 亮点 |
|------|------|
| **Why AI Agents Still Need You: Findings from Developer-Agent Collaborations in the Wild** | 开发者-Agent协作实证 |
| **Wired for Reuse: Automating Context-Aware Code Adaptation in IDEs via LLM-Based Agent** | IDE中Agent代码适配 |
| **Vul-R2: A Reasoning LLM for Automated Vulnerability Repair** | 自动化漏洞修复推理 |
| **Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation** | 多Agent协作代码审查推荐 |
| **VeriExploit: Automatic Bug Reproduction in Smart Contracts via LLMs and Formal Methods** | LLM+形式化方法 |
| **VERT: Polyglot Verified Equivalent Rust Transpilation with Large Language Models** | 多语言Rust转译 |

## ASE 2024 / ISSTA 2024 / arXiv

| 论文 | 来源 | 亮点 |
|------|------|------|
| **Prompt Sapper: LLM-Empowered Production Tool for Building AI Chains** | ASE 2024 / arXiv:2306.06548 | AI Chain构建工具 |
| **PlayCoder: Making LLM-Generated GUI Code Playable** | arXiv:2604.19742 | 多Agent生成-评估-修复GUI闭环 |
| **Chat2Workflow: A Benchmark for Generating Executable Visual Workflows with Natural Language** | arXiv:2604.19742 | NL→可视化工作流 |
| **CoqPilot: LLM-based generation of Coq proofs** | ASE 2024 | Agent辅助形式化证明 |
| **Can Cooperative Multi-Agent Reinforcement Learning Boost Automatic Web Testing?** | ASE 2024 | 多Agent强化学习测试 |
| **Refute-or-Promote: An Adversarial Stage-Gated Multi-Agent Review Methodology** | arXiv:2604.19742 | 对抗性多Agent缺陷发现 |
| **TeamFusion: Supporting Open-ended Teamwork with Multi-Agent Systems** | arXiv:2604.19742 | 开放式团队协作 |
| **Mesh Memory Protocol: Semantic Infrastructure for Multi-Agent LLM Systems** | arXiv:2604.19742 | 多Agent语义内存协议 |

## 协作模式

1. **分工协作模式**: 不同Agent负责不同子任务
2. **串行Chain模式**: Agent形成处理链，上一个Agent输出作为下一个输入
3. **并行投票模式**: 多个Agent独立处理，投票决定最终结果
4. **对抗性评审模式**: 多个Agent相互审查、反驳、促进（如Refute-or-Promote, SWE-Debate）
5. **竞争性辩论模式**: 多Agent通过辩论达成共识（如SWE-Debate）
6. **统一Agent模式**: 单个Agent承担完整软件工程任务
7. **Human-in-the-loop协作模式**: 开发者与Agent协作，人类介入决策
8. **跨语言翻译+多Agent精炼模式**: 跨语言翻译配合多Agent协同优化

## 研究趋势

1. **Multi-Agent辩论/对抗成为热点**: SWE-Debate等论文引入竞争性辩论机制
2. **统一Agent vs 多Agent分工**: 出现统一SE Agent尝试单Agent完成全部任务
3. **Human-Agent协作研究兴起**: 关注开发者与Agent的实际协作
4. **安全漏洞修复成为重要应用**: Agentic AI + OSS-Fuzz、Vul-R2等

## 核心问题

- 多个LLM Agent如何有效分工？
- 如何保证多Agent协作的一致性和可解释性？
- Agent之间的通信协议如何设计？
- 如何处理Agent协作中的错误传播？
- 多Agent系统中的角色分配和动态转换机制？

## 待确认的 arXiv 论文（需在 DBLP 验证 CCF-A 状态）

| arXiv ID | 标题 | 是否CCF-A |
|----------|------|-----------|
| 2510.03463 | ALMAS: Autonomous LLM-based Multi-Agent SE Framework | 待确认 |
| 2511.08475 | Designing LLM-based Multi-Agent Systems for SE | ICSE 2026？ |
| 2511.18467 | Shadows in the Code: Risks and Defenses of LLM Multi-Agent SD | 待确认 |
| 2404.04834 | LLM-Based Multi-Agent Systems for SE: Vision and Road Ahead | 待确认 |
| 2505.16086 | Optimizing LLM-Based Multi-Agent with Textual Feedback | 待确认 |
| 2512.21818 | Analyzing Code Injection Attacks on LLM Multi-Agent | 待确认 |

## 相关方向

- [[workflow-automation]] — AI Chain是工作流自动化的具体实现
- [[code-review-static-analysis]] — 代码审查是多Agent协作的典型场景
- [[program-repair]] — 多Agent可用于程序修复的不同阶段
- [[test-generation]] — 多Agent可分工生成测试和验证测试
- [[ICSE-2026]] — 最多multi-agent论文的会议

## ICSE 2026 Agentic Era Panels

ICSE 2026设立了多个关于Agentic时代的Panel，探讨AI Agent对软件工程的影响：

- **SE.next: In the Agentic Trenches** — 探讨Agentic工程实践
- **SE.next: Research in the Agentic Era** — Agent时代的研究方向
- **SE.next: Raising the Agentic Engineer** — 培养Agentic工程师

这些Panel反映出学术界对AI Agent改变软件工程实践的高度关注。
