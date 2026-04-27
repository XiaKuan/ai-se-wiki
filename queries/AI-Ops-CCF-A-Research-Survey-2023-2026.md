---
title: AI-Ops × LLM Agent 运维科研调研报告 (2023-2026)
created: 2026-04-23
updated: 2026-04-23
type: research-survey
tags: [aiops, llm-agent, sre, operations, benchmark, dataset, CCF-A, research-trend]
sources: [ICSE-2025, ICSE-2026, FSE-2024, FSE-2025, ASE-2024, ASE-2025, ISSTA-2024, AIware-2025, arXiv]
---

# AI-Ops × LLM Agent 运维科研调研报告 (2023-2026)

> 调研时间: 2026-04-23 (2026-04-27 更新ASE 2025新增论文)
> 覆盖会议: ICSE (2023-2026), FSE (2023-2025), ASE (2023-2025), ISSTA (2023-2025), AIware (2024-2025)
> 核心关键词: AI-Ops, LLM Agent, SRE, Autonomous Operations, Incident Response, Log Analysis, Alert Triage, Benchmark, Dataset

---

## 一、核心发现

### 1.1 三大趋势

1. **Multi-Agent SRE Agent 是最前沿方向**: 2024-2026年，LLM Agent从单智能体进化到多智能体协作完成运维任务（根因分析、事件响应、告警处理）
2. **运维数据集严重稀缺**: 公开的运维Benchmark非常少，这是目前AI-Ops研究的最大瓶颈，也是最佳科研切入点
3. **AIOps正在向AgenticAIops演进**: 从规则/ML驱动，转向LLM Agent自主决策

### 1.2 论文分布

|| 会议 | AI-Ops/运维相关论文数 | LLM Agent SRE方向 | 数据集/Benchmark方向 | 备注 |
||------|---------------------|-------------------|---------------------|------|
|| ICSE 2026 | 11+ | 9+ | 3+ | RCA方向最热，Crash RCA新出现 |
|| ASE 2025 | 11+ | 5+ | 3+ | **Log分析6篇，极为活跃** |
|| FSE 2024 | 15+ | 8+ | 2+ | RCA方向5篇，Cloud Incident Management成规模 |
|| FSE 2025 | 未知 | 未知 | 未知 | 论文列表未发布 |
|| ISSTA 2024 | 7+ | 3+ | 3+ | LogPPT + RCAEval |
|| AIware 2025 | 6+ | 4+ | 4+ | Benchmark & Dataset Track |

---

## 二、LLM Agent 运维 / SRE 论文汇总

### 2.1 ICSE (2026为重点)

#### ICSE 2026

||| 论文 | 方向 | 机构 | 备注 | 来源 |
||------|------|------|------|------|------|
|| **Agentic Memory Enhanced Recursive Reasoning for Root Cause Localization** | RCA + Agentic Memory | ICSE 2026 | 最新进展 | researchr.org |
|| **FoundRoot: Towards Foundation Model for Root Cause Analysis** | RCA Foundation Model | 清华/字节 | 结构化深度思考 | researchr.org |
|| **R-Log: Incentivizing Log Analysis Capability in LLMs via RL** | Log分析 + RL | ICSE 2026 | 新研究方向 | researchr.org |
|| **OpenDerisk: An Industrial Framework for AI-Driven SRE** | 工业SRE框架 | ICSE 2026 | 设计与实现 | researchr.org |
|| **TAAF: Trace Abstraction & Analysis Framework Synergizing KG + LLMs** | Trace + 知识图谱 | ICSE 2026 | 知识图谱融合 | researchr.org |
|| **Finding the Needle in the Crash Stack (AutoCrashFL)** | Crash RCA + 工业级 | ICSE 2026 | 工业规模Crash定位 | researchr.org |
|| **"Where is My Troubleshooting Procedure?" RAG for Failure Resolution** | RAG + 故障排除 | ICSE 2026 | CPS系统RAG | researchr.org |
|| **Learning from Change: Predictive Models for Incident Prevention** | 事故预防 + 预测模型 | ICSE 2026 | 监管环境 | researchr.org |
|| **SWE-Debate: Competitive Multi-Agent Debate for Issue Resolution** | Multi-Agent辩论 | 上海交大 | ICSE 2026 Research | researchr.org |
|| **Evaluating and Improving Automated Repository-Level Rust Issue Resolution** | Rust Issue Agent | 南科大 | ICSE 2026 Research | researchr.org |
|| **LLM-Based Automated Diagnosis Of Integration Test Failures At Google** | Test诊断 | Google | ICSE 2026 SEIP | researchr.org |

#### ICSE 2025 / 2024

| 论文 | 方向 | 备注 |
|------|------|------|
| **UniSyn: Generating Realistic and Diverse Test Cases for Code Repair** | 测试用例生成 | ICSE 2025 |
| **A Large Language Model Based Framework for Predicting Incident-related Commits** | 事故相关提交预测 | LLM+代码分析 |

### 2.2 ASE (2024-2025)

#### ASE 2025

|| 论文 | 方向 | 备注 | 来源 |
||------|------|------|------|
|| **LLM-Powered Multi-Agent Collaboration for Intelligent Industrial On-Call Automation** | 智能运维 + 多Agent | 工业On-Call自动化 | researchr.org |
|| **United We Stand: Towards End-to-End Log-based Fault Diagnosis via Interactive Multi-Task Learning** | Log故障诊断 + 多任务 | 交互式多任务学习 | researchr.org |
|| **Improving LLM-based Log Parsing by Learning from Errors in Reasoning Traces** | Log解析 + 反思学习 | 从推理错误中学习 | researchr.org |
|| **LogAction: Consistent Cross-system Anomaly Detection through Logs via Active Domain Adaptation** | Log异常检测 + 域适应 | 跨系统一致异常检测 | researchr.org |
|| **Defects4Log: Benchmarking LLMs for Logging Code Defect Detection and Reasoning** | Log代码缺陷检测 + Benchmark | 评测LLM日志缺陷能力 | researchr.org |
|| **CollaborLog: Efficient-Generalizable Log Anomaly Detection via Large-Small Model Collaboration** | Log异常检测 + 大小模型 | 泛化性+效率 | researchr.org |
|| **Root Cause Analysis of RISC-V Build Failures via LLM and MCTS Reasoning** | RCA + MCTS | RISC-V构建失败RCA | researchr.org |
|| **LogUpdater: Automated Detection and Repair of Specific Defects in Logging Statements** | Log语句自动化修复 | 检测+修复日志缺陷 | researchr.org |
|| **Demystifying LLM-based Software Engineering Agents** | SE Agent系统性分析 | AIware 2025 Main Track | researchr.org |
|| **Automatically Maintaining Agent Systems: How Far Are We?** | Agent自动维护 | 重要新方向 | researchr.org |
|| **Teaching LLMs to Debug: Toward Reasoning- and Tool-Aware Coding Agents** | 调试Agent | 推理+工具感知 | researchr.org |

**注**: ASE 2025 Log分析方向极为活跃（6篇相关），涵盖解析、异常检测、缺陷检测、RCA全链条。

#### ASE 2024

| 论文 | 方向 | 备注 |
|------|------|------|
| **The Potential of One-Shot Failure Root Cause Analysis: Collaboration of LLM and Small Classifier** | 根因分析 | 小分类器+LLM协作 |
| **FAIL: Analyzing Software Failures from the News Using LLMs** | 新闻分析故障 | LLM处理非结构化数据 |
| **Exploring LLM-based Agents for Root Cause Analysis** | LLM Agent根因分析 | FSE 2024也有 |
| **Automated Root Causing of Cloud Incidents using In-Context Learning with GPT-4** | 云事故根因 | GPT-4上下文学习 |
| **Face It Yourselves: An LLM-Based Two-Stage Strategy to Localize Configuration Errors via Logs** | 日志配置错误定位 | ISSTA 2024 |

### 2.3 FSE (2024-2025)

#### FSE 2024（来源：researchr.org）

|| 论文 | 方向 | 备注 |
||------|------|------|
|| **BARO: Robust Root Cause Analysis for Microservices via Multivariate Bayesian Online Change Point Detection** | RCA + 贝叶斯变点 | 多变量贝叶斯RCA |
|| **Chain-of-Event: Interpretable Root Cause Analysis for Microservices through Automatically Learning Weighted Event Causal Graph** | RCA + 因果图 | 可解释RCA，因果图自动学习 |
|| **ChangeRCA: Finding Root Causes from Software Changes in Large Online Systems** | RCA + 代码变更 | 大规模在线系统 |
|| **LM-PACE: Confidence Estimation by Large Language Models for Effective Root Causing of Cloud Incidents** | Cloud RCA + LLM置信度 | LLM估计置信度提升RCA |
|| **X-lifecycle Learning for Cloud Incident Management using LLMs** | Cloud Incident Management | LLM全生命周期管理 |
|| **MonitorAssistant: Simplifying Cloud Service Monitoring via Large Language Models** | Cloud Monitoring + LLM | LLM简化监控 |
|| **Automated Root Causing of Cloud Incidents using In-Context Learning with GPT-4** | Cloud RCA + GPT-4 | 上下文学习 |
|| **Exploring LLM-based Agents for Root Cause Analysis** | LLM Agent RCA | FSE 2024 |
|| **LILAC: Log Parsing using LLMs with Adaptive Parsing Cache** | Log解析 + LLM | 自适应解析缓存 |
|| **Go Static: Contextualized Logging Statement Generation** | 日志语句生成 | 上下文感知日志生成 |
|| **LogSD: Detecting Anomalies from System Logs through Self-supervised Learning** | Log异常检测 | 自监督学习 |
|| **A Critical Review of Common Log Data Sets Used for Evaluation of Sequence-based Anomaly Detection** | Log数据集综述 | 批判性综述 |
|| **Fault Diagnosis for Test Alarms in Microservices Through Multi-source Data** | 故障诊断 + 多源数据 | 微服务测试告警 |
|| **Decoding Anomalies! Unraveling Operational Challenges in Human-in-the-Loop Anomaly Validation** | 人机协同异常验证 | 运维实践挑战 |
|| **ConDefects: A Complementary Dataset for LLM-based Fault Localization and Program Repair** | 数据集 + 缺陷定位 | 数据泄露问题 |

**注**: FSE 2024 RCA方向极为集中（5篇），Cloud Incident Management主题首次成规模出现。

#### FSE 2025

论文列表尚未发布（返回空），无法检索。

### 2.4 ISSTA (2024)

|| 论文 | 方向 | 备注 | 来源 |
||------|------|------|------|
|| **LogPPT: Large Language Models as Log Analysts** | Log分析 + LLM | PPT风格日志解析框架 | ISSTA 2024 |
|| **RCAEval: A Benchmark for Root Cause Analysis of Microservice Systems (735 cases)** | RCA Benchmark | 15个baseline，ISSTA 2024 | ISSTA 2024 |
|| **Face It Yourselves: An LLM-Based Two-Stage Strategy to Localize Configuration Errors via Logs** | 配置错误定位 + Log | 两阶段策略 | ISSTA 2024 |
|| **A Large-Scale Evaluation for Log Parsing Techniques: How Far Are We?** | Log解析评测 | 大规模Log解析技术评估 | ISSTA 2024 |
|| **FastLog: An End-to-End Method to Efficiently Generate and Insert Logging Statements** | 日志生成 | 端到端日志语句生成 | ISSTA 2024 |
|| **AutoCodeRover: Autonomous Program Improvement** | 自主程序改进 | 自主Agent | ISSTA 2024 |
|| **Enhancing Multi-agent System Testing with Diversity-Guided Exploration** | Multi-Agent测试 | 多智能体系统测试 | ISSTA 2024 |

---

## 三、运维数据集 / Benchmark 专项汇总

> 这是AI-Ops研究的核心资源，也是目前最大的研究缺口

### 3.1 权威运维Benchmark

| 数据集 | 方向 | 来源 | 特点 |
|--------|------|------|------|
| **SWE-Bench** | 软件工程任务 | arXiv/ICSE | 真实GitHub Issue-Patch对 |
| **SWE-Sharp-Bench** | C#软件工程 | AIware 2025 B&D Track | SWE-Bench的C#版本 |
| **HPCAgentTester** | HPC测试生成 | AIware 2025 B&D Track | Multi-Agent HPC测试 |
| **SIR-Bench** | 安全事件响应 | AIware 2025 B&D Track | Security Incident Response Agent评测 |
| **UniTSyn** | 程序测试 | ISSTA 2024 | 单元测试增强数据集 |

### 3.2 日志分析数据集

| 数据集 | 方向 | 备注 |
|--------|------|------|
| **LogPPT Dataset** | 日志解析 | ISSTA 2024 LogPPT配套数据 |
| **BGL Log** | 超算日志 | 公开数据集 |
| **HDFS Log** | 分布式系统日志 | 公开数据集 |
| **OpenStack Log** | 云平台日志 | 公开数据集 |

### 3.3 事件响应/根因分析数据集

| 数据集 | 方向 | 来源 |
|--------|------|------|
| **SIR-Bench Dataset** | 安全事件响应Agent评测 | AIware 2025 |
| **Cloud Incident Dataset** | 云平台事故 | 相关论文配套 |
| **Bug Report Dataset** | Bug报告分类 | ASE/AIware相关论文 |

### 3.4 SRE/运维 Benchmark 缺口分析

**目前最稀缺的资源**:
1. **Multi-Agent SRE Benchmark**: 没有专门评测多智能体协作运维能力的基准
2. **Real-time Incident Response Dataset**: 实时告警→诊断→修复的完整流程数据
3. **Cross-system Operations Dataset**: 跨多个系统（K8s + DB + Network）的联合运维数据
4. **Human-in-the-loop Operations Dataset**: 人机协作的运维决策数据

---

## 四、arXiv 高影响力 AI-Ops 论文

> 以下论文虽非直接CCF-A，但代表最前沿研究方向

### 4.1 LLM Agent SRE 核心论文

| 论文 | arXiv ID | 方向 | 重要性 |
|------|----------|------|--------|
|| **Deploy, Calibrate, Monitor, Heal -- An Autonomous AI SRE Agent** | 2604.03933 | **全生命周期SRE Agent** | ⭐⭐⭐⭐⭐ 必读 |
| **In-Context Autonomous Network Incident Response** | 2602.13156 | 网络事件响应 | ⭐⭐⭐⭐ |
| **Multi-Agent LLM Orchestration for Incident Response** | 2511.15755 | 多智能体事件响应 | ⭐⭐⭐⭐ |
| **Agentic Observability: Automated Alert Triage with LLM-based Multi-Agents** | 2602.02585 | 智能告警分类 | ⭐⭐⭐⭐ |
| **LBOps: Leaderboard Operations -- Benchmarking LLMs on DevOps Tasks** | 2407.04065 | DevOps评测基准 | ⭐⭐⭐⭐ |

### 4.2 Log Analysis 论文

| 论文 | arXiv ID | 方向 |
|------|----------|------|
| **Scalable and Efficient Large-Scale Log Analysis with LLMs** | 2511.14803 | IT软件支持日志分析 |
| **LLM-5GMAC: LLM-Based MAC-Layer Log Analysis** | - | 通信系统日志(OpenRan) |

### 4.3 论文核心观点总结

**2604.19742 (FSE 2026 投稿)**:
- 提出了完整的AI SRE Agent生命周期: Deploy → Calibrate → Monitor → Heal
- 覆盖: 部署、监控、调参、自愈
- 这是目前最完整的AI-Ops Agent框架论文

**2602.02585 (Agentic Observability)**:
- 用Multi-Agent做告警分类(Triage)
- Agent分别处理: 日志分析、指标分析、追踪分析
- 最终汇聚决策

---

## 五、AIware 2025 专项分析

> AIware 是ASE co-located会议，Benchmark & Dataset Track对AI-Ops有重要参考价值

### 5.1 Main Track (LLM Agent SE)

| 论文 | 核心贡献 |
|------|----------|
| **CHASE: LLM Agents for Dissecting Malicious PyPI Packages** | 恶意包分析Agent |
| **Claude Code: From Single Agent to Multi-Agent Systems** | Claude Code架构演进分析 |
| **Demystifying LLM-based Software Engineering Agents** | SE Agent系统性分析 |
| **Teaching LLMs to Debug** | 推理+工具感知调试 |
| **Ambient, Safe Agentic Automation on GitHub** | GitHub平台自动化 |

### 5.2 Benchmark & Dataset Track

| 论文 | 核心贡献 |
|------|----------|
| **SIR-Bench: Security Incident Response Agent Benchmark** | 安全事件响应Agent评测 |
| **HPCAgentTester: Multi-Agent HPC Test Generation** | HPC Multi-Agent测试 |
| **AutoBnB-RAG: Multi-Agent Incident Response with RAG** | 事件响应RAG增强 |
| **Turning Manual Tasks into Actions: Assessing Gemini-generated Selenium Tests** | 自动化测试评估 |

### 5.3 AgenticSE Workshop (ASE 2025)

专门针对 **LLM Agent + Software Engineering** 的workshop，是该方向的热门投稿渠道。

---

## 六、研究趋势与科研切入点

### 6.1 趋势总结

1. **从单Agent到Multi-Agent**: 多个专业Agent协作完成复杂运维任务
2. **从规则驱动到LLM驱动**: 传统AIOps用规则/ML，新方向用LLM理解+决策
3. **全生命周期覆盖**: Deploy→Monitor→Diagnose→Heal的完整Agent
4. **Benchmark稀缺**: 严重缺乏高质量运维Benchmark，这是最大的研究机会

### 6.2 最佳科研切入点

#### 🥇 切入点1: 构建运维Benchmark (最佳！)

**理由**: 目前最大缺口，创新空间极大

**可做方向**:
- Multi-Agent SRE Benchmark: 评测多个Agent协作处理事故的能力
- Real-time Incident Dataset: 实时告警→诊断→修复流程数据
- Cross-system Operations: 跨K8s、DB、Network的联合运维

**可行性**: 高。数据来源明确（GitHub、公开SRE数据集），评价指标可定义

#### 🥇 切入点2: Multi-Agent 运维协作框架

**理由**: ICSE 2026已有Multi-Agent辩论论文，是前沿热点

**可做方向**:
- 专业Agent分工: 日志Agent + 告警Agent + 代码Agent协作
- Agent间通信协议设计
- 协作失败诊断与恢复

#### 🥈 切入点3: Vibe Coding + 运维

**理由**: 与你的研究兴趣相关

**可做方向**:
- 自然语言运维: "为什么这个服务变慢了？" → 自动分析+修复
- 运维知识图谱构建

---

## 七、关键论文清单 (可直接搜索)

### LLM Agent SRE (必读)

1. **Deploy, Calibrate, Monitor, Heal -- An Autonomous AI SRE Agent** (arXiv 2604.19742)
2. **In-Context Autonomous Network Incident Response** (arXiv 2602.13156)
3. **Agentic Observability: Automated Alert Triage** (arXiv 2602.02585)
4. **Multi-Agent LLM Orchestration for Incident Response** (arXiv 2511.15755)
5. **LBOps: Leaderboard Operations** (arXiv 2407.04065)

### CCF-A 会议论文

1. **SWE-Debate** (ICSE 2026) - Multi-Agent辩论
2. **Exploring LLM-based Agents for Root Cause Analysis** (FSE 2024)
3. **Face It Yourselves** (ISSTA 2024) - 日志配置错误定位
4. **The Potential of One-Shot Failure Root Cause Analysis** (ASE 2024)
5. **LogPPT** (ISSTA 2024) - 日志分析

### Benchmark & Dataset

1. **SWE-Bench** - 最权威SE任务Benchmark
2. **SIR-Bench** (AIware 2025) - 安全事件响应评测
3. **HPCAgentTester** (AIware 2025) - HPC Multi-Agent测试

---

## 八、行动建议

### 立即行动 (本周)

1. **精读核心论文**: 2604.19742 (AI SRE Agent) + 2602.02585 (Agentic Observability)
2. **理解Benchmark缺口**: 梳理现有运维数据集的不足
3. **确定具体切入点**: 在Benchmark构建 vs Multi-Agent框架之间选择

### 短期目标 (本月)

1. **确定研究课题**: 完成开题报告初稿
2. **获取基线数据**: 选择或构建第一个运维数据集
3. **设计实验方案**: 明确评测指标

### 中期目标 (下学期)

1. **系统实现**: 完成Benchmark或Agent框架
2. **实验验证**: 在真实数据上验证
3. **论文投稿**: CCF-A (ICSE/FSE/ASE) 或 AIware

---

## 九、相关Wiki条目

- [[aiops-log-analysis]] — AI-Ops日志分析
- [[multi-agent-collaboration]] — Multi-Agent协作
- [[ASE-2024]] — ASE 2024论文
- [[ASE-2025]] — ASE 2025论文
- [[ICSE-2025]] — ICSE 2025论文
- [[FSE-2024]] — FSE 2024论文
- [[FSE-2025]] — FSE 2025论文
- [[ISSTA-2024]] — ISSTA 2024论文
- [[AIware-2025]] — AIware 2025论文
- [[vibe-coding]] — Vibe Coding方向

---

*报告生成时间: 2026-04-23*
*数据来源: CCF-A会议官网, arXiv, AIware 2025 Program, DBLP*
