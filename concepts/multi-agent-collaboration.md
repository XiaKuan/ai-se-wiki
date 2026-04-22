---
title: Multi-Agent Collaboration (多LLM Agent协作系统)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [multi-agent, CCF-A, LLM, workflow-automation, research-trend, ASE-2024, ASE-2025, ICSE-2026, ISSTA-2024]
sources: [ASE-2024, ASE-2025, ICSE-2026, ISSTA-2024, arXiv]
---

## 定义

多LLM Agent协作系统指多个大语言模型Agent协同工作，共同完成复杂软件工程任务的系统范式。这是2024年新爆发的研究方向，代表了从"LLM as Tool"到"LLM as Collaborator"的范式转变。

## 研究现状

### 核心论文 (CCF-A + arXiv)

#### ICSE 2026 (2026年4月, 里约热内卢) — CCF-A

| 论文 | 亮点 |
|------|------|
| **SWE-Debate: Competitive Multi-Agent Debate for Software Issue Resolution** | 多Agent辩论解决软件问题，对抗性协作 |
| **Unified Software Engineering Agent as AI Software Engineer** | 统一Agent作为AI软件工程师 |
| **Unlocking LLM Repair Capabilities Through Cross-Language Translation and Multi-Agent Refinement** | 跨语言+多Agent协同修复 |
| **Evaluating and Improving Automated Repository-Level Rust Issue Resolution with LLM-based Agents** | LLM-based Agents自动化Rust issue解决 |
| **More with Less: An Empirical Study of Turn-Control Strategies for Efficient Coding Agents** | 高效编码Agent的轮次控制策略 |
| **Fixing Security Vulnerabilities with Agentic AI in OSS-Fuzz** | Agentic AI在OSS-Fuzz中修复安全漏洞 |
| **CREME: Robustness Enhancement of Code LLMs via Layer-Aware Model Editing** | 代码LLM鲁棒性增强 |

#### ASE 2025 (2025年11月, 首尔) — CCF-A

| 论文 | 亮点 |
|------|------|
| **Why AI Agents Still Need You: Findings from Developer-Agent Collaborations in the Wild** | 开发者-Agent协作实证研究 |
| **Wired for Reuse: Automating Context-Aware Code Adaptation in IDEs via LLM-Based Agent** | IDE中基于Agent的上下文感知代码适配 |
| **Vul-R2: A Reasoning LLM for Automated Vulnerability Repair** | 自动化漏洞修复推理LLM |
| **Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation** | 多Agent协作代码审查推荐 |
| **VeriExploit: Automatic Bug Reproduction in Smart Contracts via LLMs and Formal Methods** | LLM+形式化方法自动复现智能合约bug |
| **VERT: Polyglot Verified Equivalent Rust Transpilation with Large Language Models** | LLM多语言验证等效Rust转译 |

#### ASE 2024 / ISSTA 2024 / arXiv

| 论文 | 会议/来源 | 亮点 |
|------|----------|------|
| **Prompt Sapper: LLM-Empowered Production Tool for Building AI Chains** | ASE 2024 / arXiv:2306.06548 | AI Chain构建工具，no-code IDE |
| **PlayCoder: Making LLM-Generated GUI Code Playable** | arXiv:2604.19742 | 多Agent生成-评估-修复GUI代码闭环 |
| **Chat2Workflow: A Benchmark for Generating Executable Visual Workflows with Natural Language** | arXiv:2604.19742 | 自然语言生成可视化工作流 |
| **CoqPilot: LLM-based generation of Coq proofs** | ASE 2024 | Agent辅助形式化证明 |
| **Can Cooperative Multi-Agent Reinforcement Learning Boost Automatic Web Testing?** | ASE 2024 | 多Agent强化学习网页测试 |
| **Refute-or-Promote: An Adversarial Stage-Gated Multi-Agent Review Methodology for High-Precision LLM-Assisted Defect Discovery** | arXiv:2604.19742 | 对抗性多阶段多Agent缺陷发现 |
| **TeamFusion: Supporting Open-ended Teamwork with Multi-Agent Systems** | arXiv:2604.19742 | 开放式团队协作多Agent系统 |
| **Mesh Memory Protocol: Semantic Infrastructure for Multi-Agent LLM Systems** | arXiv:2604.19742 | 多Agent系统的语义内存协议 |

### 协作模式 (2025-2026年扩展)

1. **分工协作模式**: 不同Agent负责不同子任务（如一个负责代码生成，一个负责测试验证）
2. **串行Chain模式**: Agent形成处理链，上一个Agent输出作为下一个输入
3. **并行投票模式**: 多个Agent独立处理，投票决定最终结果
4. **对抗性评审模式**: 多个Agent相互审查、反驳、促进（如Refute-or-Promote, SWE-Debate）
5. **竞争性辩论模式 (新增)**: 多Agent通过辩论达成共识（如SWE-Debate）
6. **统一Agent模式 (新增)**: 单个Agent承担完整软件工程任务（如Unified SE Agent）
7. **Human-in-the-loop协作模式 (新增)**: 开发者与Agent协作，人类介入决策（如Why AI Agents Still Need You）
8. **跨语言翻译+多Agent精炼模式 (新增)**: 跨语言翻译配合多Agent协同优化（如Unlocking LLM Repair）

### 研究趋势

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

## 代表性论文详解

### ICSE 2026 新增论文

#### 1. SWE-Debate (ICSE 2026)
**竞争性多Agent辩论解决软件问题**

- **核心贡献**: 提出SWE-Debate框架，通过竞争性多Agent辩论解决软件issue
- **方法**: 多Agent相互辩论，最终达成共识或选出最优解决方案
- **作者**: Han Li, Yuling Shi, Shaoxin Lin, Xiaodong Gu等 (上海交大, 华为)

#### 2. Unified Software Engineering Agent (ICSE 2026)
**统一Agent作为AI软件工程师**

- **核心贡献**: 探索将单一Agent打造为完整的AI软件工程师
- **方法**: Agent承担从需求到代码的全流程任务
- **作者**: Leonhard Applis, Yuntong Zhang, Shanchao Liang, Lin Tan, Abhik Roychoudhury等

#### 3. Why AI Agents Still Need You (ASE 2025)
**开发者-Agent协作实证研究**

- **核心贡献**: 首次大规模研究实际开发环境中开发者与AI Agent的协作模式
- **发现**: 当前AI Agent仍需要人类介入，开发者角色不可替代
- **实践意义**: 为Human-in-the-loop Agent系统设计提供指导

#### 4. Unlocking LLM Repair Through Cross-Language + Multi-Agent (ICSE 2026)
**跨语言翻译+多Agent精炼**

- **核心贡献**: 利用跨语言翻译增强LLM修复能力
- **方法**: 多个Agent协同精炼翻译后的代码

### arXiv 2026年论文

#### 5. PlayCoder (arXiv, 2026)
**多Agent闭环GUI代码生成-评估-修复框架**

- **核心贡献**: 提出PlayEval基准测试和Play@k指标，评估GUI应用的可执行性和逻辑正确性
- **方法**: PlayCoder多Agent框架，包含生成Agent、测试Agent、修复Agent
- **关键发现**: 即使编译通过，当前LLM在Play@3上接近0，说明传统指标不足以评估GUI应用
- **性能**: PlayCoder将Exec@3提升至38.1%，Play@3提升至20.3%

#### 6. Chat2Workflow (arXiv, 2026)
**自然语言生成可执行可视化工作流**

- **核心贡献**: 提出Chat2Workflow基准，从自然语言生成可在Dify/Coze等平台部署的工作流
- **挑战**: LLM能捕捉高层意图，但难以生成正确、稳定、可执行的工作流
- **方法**: 提出agentic框架缓解执行错误，resolve rate提升5.34%

#### 7. Refute-or-Promote (arXiv, 2026)
**对抗性阶段门控多Agent评审方法**

- **核心贡献**: 高精度LLM辅助缺陷发现的多Agent评审方法
- **方法**: 包含多轮对抗性评审，Agent相互反驳或促进候选发现

#### 8. Unity Is Strength (ASE 2024/2025)
**协作式LLM Agent代码审查者推荐**

- **核心思想**: 多个LLM Agent协作完成代码审查者推荐任务

## 相关方向

- [[workflow-automation]] — AI Chain是工作流自动化的具体实现
- [[code-review-static-analysis]] — 代码审查是多Agent协作的典型场景
- [[program-repair]] — 多Agent可用于程序修复的不同阶段
- [[test-generation]] — 多Agent可分工生成测试和验证测试

## ICSE 2026 Agentic Era Panels

ICSE 2026设立了多个关于Agentic时代的Panel，探讨AI Agent对软件工程的影响：

- **SE.next: In the Agentic Trenches** — 探讨Agentic工程实践
- **SE.next: Research in the Agentic Era** — Agent时代的研究方向
- **SE.next: Raising the Agentic Engineer** — 培养Agentic工程师

这些Panel反映出学术界对AI Agent改变软件工程实践的高度关注。
