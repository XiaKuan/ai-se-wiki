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

## 效果评估方法（Evaluation Methods）

### 论文类型与评估性质

| 论文 | 类型 | 评估性质 |
|------|------|----------|
| 2511.08475 (Designing Multi-Agent) | Survey/文献综述 | 质性分析，无实证评估 |
| 2404.04834 (Vision and Road Ahead) | Survey/系统性综述 | 质性分析 + 案例演示 |
| 2510.03463 (ALMAS) | Framework proposal | 案例演示，**无量化评估** |
| 2511.18467 (Shadows) | Security攻击/防御研究 | 量化实验 |
| 2505.16086 (Optimizing Multi-Agent) | 优化方法研究 | 多维量化实验 |
| 2512.21818 (Code Injection) | 安全架构研究 | 量化实验 |

### 评估维度分类

#### 1. 任务完成类（最常用）

| 指标 | 论文 | 说明 |
|------|------|------|
| **Pass@k** (k=1,10,100) | 2512.21818, 2505.16086 | 代码生成通过率，k次采样至少1次通过 |
| **Attack Success Rate (ASR)** | 2511.18467, 2512.21818 | 恶意行为达成率（越低越好） |
| **Benign Utility (BU)** | 2511.18467 | 正常任务完成能力 |
| **Utility Under Attack (UUA)** | 2511.18467 | 被攻击后正常任务完成能力 |
| **Reject Rate (RR)** | 2511.18467 | 系统拒绝恶意请求率 |
| **Accuracy** | 2512.21818 | 架构被攻击后的正确性 |

#### 2. 效率类

| 指标 | 论文 | 说明 |
|------|------|------|
| **LLM Call数量** | 2512.21818 | 架构效率（coder: 164 calls, coder-reviewer-tester更多） |
| Token消耗 | — | 未被明确报告 |
| 响应时间 | — | 未被明确报告 |

#### 3. 协作质量类（最关键、最空白）

> **2511.08475 (Survey, 94篇论文) 明确指出**：
> *"lack of objective evaluation metrics for multi-agent collaboration quality"* — 这是multi-agent研究最大挑战

| 论文 | 涉及内容 | 局限 |
|------|----------|------|
| 2505.16086 | "Group behavior"分析 | 用文本反馈识别欠佳Agent，但**无统一协作质量指标** |
| 2511.08475 | 16种设计模式 | Survey发现没有系统性的协作质量量化方法 |

#### 4. 安全性类（仅安全相关论文）

| 指标 | 说明 |
|------|------|
| ASR | 攻击成功率，越低越好 |
| ASR-d | 防御后的攻击成功率 |
| RR | 系统拒绝恶意请求率 |
| BU | 正常用户任务的完成质量 |
| UUA | 被攻击干扰后仍正常工作的能力 |

### 核心结论：是否存在客观量化方法？

**有，但碎片化、无统一标准：**

1. **任务级指标**（Pass@k、Accuracy）— 借用单Agent评估，**无法衡量协作本身**
2. **安全指标**（ASR/BU/RR）— 只在安全场景有效
3. **效率指标**（LLM calls）— 只衡量计算成本，不衡量质量
4. **协作质量指标**— **几乎空白**，是最大研究gap

### 关键研究空白（科研机会）

| Gap | 说明 |
|-----|------|
| **无统一协作质量基准** | 如何衡量"两Agent分工协作"优于"单Agent独立完成"？ |
| **无Role Assignment评估框架** | 不同角色分配对任务完成的影响无法量化对比 |
| **无Communication Protocol评估** | Agent间通信效率没有客观指标 |
| **无错误传播评估** | 多Agent中某Agent犯错，如何量化其对最终输出的影响？ |
| **无动态协作评估** | Agent间动态角色切换无法被现有指标捕捉 |

---

## 使用的数据集

### 数据集汇总

| 数据集 | 论文 | 规模 | 用途 |
|--------|------|------|------|
| **HumanEval** | 2512.21818, 2505.16086 | 164道Python编程题 | 代码生成能力评估 |
| **SWE-bench** | 2510.03463 (计划), 2505.16086 | 数百道真实GitHub issue修复 | 真实软件bug修复 |
| **SRDD** | 2511.18467, 2505.16086 | 1,200个软件任务prompt，40子类 | Agent驱动的软件开发 |
| **自定义480测试集** | 2511.18467 | 480个（40×5组合） | 安全攻击评估 |
| **MMLU / MATH** | 2505.16086 | 标准NLP benchmark | 与传统NLP任务对比 |

### 核心数据集详解

#### HumanEval（最常用）
- **来源**: Chen et al. (2021) "Evaluating Large Language Models Trained on Code"
- **规模**: 164道手写Python编程问题
- **结构**: 函数签名 + docstring + 测试用例
- **指标**: Pass@1 / Pass@k
- **Multi-Agent中的表现**: MetaGPT 85.9%, MapCoder(7B) 57.6%, AgentCoder +29.9% vs 单LLM
- **局限**: 单函数级别代码补全，**无法评估复杂SE任务和多Agent协作**

#### SWE-bench
- **来源**: 真实GitHub仓库issue修复
- **特点**: 需要理解代码库结构、定位bug、生成修复
- **现状**: 很多multi-agent论文**只报告HumanEval**，因为SWE-bench太难
- **ALMAS (2510.03463)**: 计划使用但**尚未完成评估**

#### SRDD (Software Requirement Description Dataset)
- **来源**: Qian et al. (2024) — ChatGPT生成
- **规模**: 1,200个软件任务prompts
- **分类**: 5大类（education/work/life/game/creation）× 40个子类
- **意义**: **目前最专门针对agent驱动软件开发**的数据集
- **2511.18467用法**: 40个子类各选1个benign任务 × 5种恶意软件行为(Trojan/Spyware/Adware/Ransomware/Virus) = 480测试用例

### 数据集使用总体问题

| 问题 | 说明 |
|------|------|
| **重代码生成，轻协作** | HumanEval/SWE-bench都是单Agent任务，无法评估Multi-Agent协作 |
| **缺乏端到端SE数据集** | SRDD最接近，但源自LLM生成（非真实需求） |
| **缺乏跨任务类型** | 少有需求工程、架构设计、测试生成等SE全生命周期任务 |
| **评估与真实场景脱节** | 164道编程题 vs 真实SE：需求→设计→实现→测试→部署 |
| **无标准化协作benchmark** | 没有专门评估multi-agent协作质量的基准 |

### 科研机会

1. **专门评估Multi-Agent协作质量的benchmark** — 不评估单Agent代码生成，而是评估：
   - Agent间任务分配合理性
   - 通信协议效率
   - 错误传播与恢复
   - Role Assignment的影响
2. **SRDD可作为构建协作benchmark的基础**（1,200个prompt × 多维度标注）
3. **端到端SE任务数据集** — 从需求到部署的全流程评估，目前几乎是空白

---

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
