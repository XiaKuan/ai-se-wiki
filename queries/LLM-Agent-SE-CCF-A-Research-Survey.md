# LLM Agent × 软件工程 CCF-A 会议科研趋势调研报告

> 调研时间: 2026-04-22
> 覆盖会议: ASE 2024, FSE 2024, ISSTA 2024 (均为CCF-A)
> 核心关键词: LLM Agent, Vibe Coding, Multi-Agent, 软件工程自动化

---

## 一、核心发现：2024年是LLM Agent爆发元年

### 标志性数据

| 指标 | ASE 2024 | FSE 2024 | ISSTA 2024 |
|------|----------|----------|-------------|
| LLM相关论文占比 | ~20% (30+/150+) | ~15% | ~20% |
| Multi-Agent论文 | 3+篇 | 2+篇 | 1+篇 |
| Test Generation方向 | 10+篇 | 5+篇 | 8+篇 |
| 代码质量/审查方向 | 5+篇 | 4+篇 | 3+篇 |

### 核心洞察

**1. 从"LLM as Tool"到"LLM as Agent"的范式转变正在发生**

传统观点将LLM视为辅助工具，但2024年的论文显示，**多个LLM Agent协作**已经成为新的研究方向：

- **Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation** (ASE 2024)
  - 多Agent协作做代码审查推荐
  - Agent之间有分工、有协作、有通信协议

- **Can Cooperative Multi-Agent Reinforcement Learning Boost Automatic Web Testing?** (ASE 2024)
  - 多Agent强化学习做Web自动化测试
  - 探索了Agent之间的协同决策机制

**2. Vibe Coding（自然语言编程）成为新兴研究方向**

用户用自然语言描述需求，AI生成完整代码——这正在从概念走向现实：

- **Self-collaboration Code Generation via ChatGPT** (ASE 2024)
  - ChatGPT自我协作生成代码
  - 一个Agent生成，另一个Agent审查和改进

- **Getting Inspiration for Feature Elicitation: App Store- vs. LLM-based Approach** (ASE 2024)
  - LLM从App Store获取灵感做需求获取
  - 探索自然语言需求→代码的转化

**3. AI Chain/Workflow Automation成为工程化落地关键**

- **Prompt Sapper: A LLM-Empowered Production Tool for Building AI Chains** (ASE 2024) ⭐
  - 构建AI链的工具
  - 把多个LLM调用串联成可执行工作流

- **LLM4Workflow: An LLM-based Automated Workflow Model Generation Tool** (ASE 2024)
  - 用LLM自动生成工作流模型
  - 从自然语言描述生成DevOps工作流

---

## 二、详细研究方向分析

### 方向1: Multi-Agent Collaboration (多Agent协作) ⭐⭐⭐⭐⭐

**推荐指数**: ★★★★★ | **创新空间**: 极高 | **竞争程度**: 较少

这是2024年最明显的新兴方向。从"单LLM工具调用"进化到"多LLM Agent协作"，代表范式转变。

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation | ASE 2024 | 多Agent协作推荐代码审查者 |
| Can Cooperative Multi-Agent Reinforcement Learning Boost Automatic Web Testing? | ASE 2024 | 多Agent强化学习Web测试 |
| Self-collaboration Code Generation via ChatGPT | ASE 2024 | Agent自我协作代码生成 |

**待解决问题**:
- Agent之间的通信协议设计
- 多Agent任务的分解与协调机制
- Agent协作的一致性和正确性保证
- 实时反馈和错误恢复机制

**你的潜在切入点**:
- **Vibe Coding + Multi-Agent**: 多Agent协作做自然语言编程，每个Agent负责不同阶段（需求理解、代码生成、测试、审查）
- **多Agent协作的可解释性**: 当多个Agent协作失败时，如何诊断问题？

---

### 方向2: Vibe Coding 质量评估 ⭐⭐⭐⭐

**推荐指数**: ★★★★☆ | **创新空间**: 极高 | **竞争程度**: 较少

**定义**: Vibe Coding = 用户用自然语言描述需求，AI系统自动生成完整代码。用户关注"做什么"而非"怎么做"。

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| Self-collaboration Code Generation via ChatGPT | ASE 2024 | 自我协作代码生成 |
| PlayCoder: Making LLM-Generated GUI Code Playable | ASE/arXiv | GUI代码可执行性 |
| Self-Elicitation of Requirements with Automated GUI Prototyping | ASE 2024 | 需求自动原型生成 |

**待解决问题**:
- 如何评估Vibe Coding生成的代码质量？（目前没有系统性框架）
- 自然语言描述和生成代码之间的语义一致性验证
- 开发者如何有效纠错和反馈？
- 生成代码的可维护性风险

**你的潜在切入点**:
- **Vibe Coding质量评估框架**: 多维度评估（功能正确性、代码可读性、安全性、性能）
- **Vibe Coding的错误模式分析**: 什么类型的自然语言描述容易导致错误的代码？

---

### 方向3: LLM Agent 安全对抗 ⭐⭐⭐⭐

**推荐指数**: ★★★★☆ | **创新空间**: 高 | **社会重要性**: 极高

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| Imperceptible Content Poisoning in LLM-Powered Applications | ASE 2024 | LLM应用的内容投毒攻击 |
| Attacking and Defending Large Language Models on Coding Tasks | ASE 2024 | 代码任务的对抗攻防 |
| Human-Imperceptible Retrieval Poisoning Attacks in LLM-Powered Applications | FSE 2024 | 检索投毒攻击 |
| CoSec: On-the-Fly Security Hardening of Code LLMs | ISSTA 2024 | 代码LLM安全加固 |
| AdvSCanner: Generating Adversarial Smart Contracts to Exploit Reentrancy Vulnerabilities | ASE 2024 | 对抗性智能合约生成 |

**待解决问题**:
- 如何检测和防御对LLM Agent的对抗性攻击？
- LLM Agent的输入验证和输出过滤
- 多Agent系统中的安全信任边界

---

### 方向4: 测试生成 (Test Generation) ⭐⭐⭐⭐

**推荐指数**: ★★★★☆ | **创新空间**: 高 | **实用性**: 极强

这是最成熟的方向之一，已有大量CCF-A论文，但仍有创新空间。

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| Towards Understanding the Effectiveness of Large Language Models on Directed Test Input Generation | ASE 2024 ⭐ Distinguished Paper | LLM测试输入生成效果理解 |
| Evaluating and Improving ChatGPT for Unit Test Generation | FSE 2024 | ChatGPT单元测试生成评估 |
| UniTSyn: Large-Scale Dataset for Enhancing LLM for Program Testing | ISSTA 2024 | 测试增强的大规模数据集 |
| Domain Adaptation for Code Model-Based Unit Test Case Generation | ISSTA 2024 | 领域自适应测试生成 |
| SlicePromptTest4J: High-coverage Test Generation using LLM via Method Slicing | ASE 2024 | 方法切片指导的高覆盖测试生成 |

**待解决问题**:
- 如何提高LLM生成测试的覆盖率？
- 测试预言(Test Oracle)的自动生成
- 模糊测试(Fuzzing) + LLM的结合

---

### 方向5: 代码质量与审查 ⭐⭐⭐

**推荐指数**: ★★★☆☆ | **创新空间**: 中高 | **实用性**: 强

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| iSMELL: Assembling LLMs with Expert Toolsets for Code Smell Detection | ASE 2024 | 工具集成代码气味检测 |
| CORE: Resolving Code Quality Issues Using LLMs | FSE 2024 | LLM解决代码质量问题 |
| Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation | ASE 2024 | 多Agent代码审查推荐 |
| Large Language Models Can Connect the Dots: Model Optimization Bugs | ISSTA 2024 | 深度学习模型优化bug发现 |

---

### 方向6: 程序理解与摘要 ⭐⭐⭐

**推荐指数**: ★★★☆☆ | **创新空间**: 中 | **基础性**: 强

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| NativeSummary: Summarizing Native Binary Code for Android Static Analysis | ISSTA 2024 | 二进制代码摘要 |
| SelfPiCo: Self-Guided Partial Code Execution with LLMs | ISSTA 2024 | 部分代码执行理解 |
| LPR: Large Language Models-Aided Program Reduction | ISSTA 2024 | 程序归约辅助 |
| Distilled GPT for source code summarization | ASE 2024 | 代码摘要蒸馏 |

---

### 方向7: 程序修复 (Program Repair) ⭐⭐⭐

**推荐指数**: ★★★☆☆ | **创新空间**: 中高 | **评价明确性**: 高

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| One Size Does Not Fit All: Multi-granularity Patch Generation | ISSTA 2024 ⭐ Distinguished Paper | 多粒度补丁生成 |
| CREF: An LLM-Based Conversational Software Repair Framework | ISSTA 2024 | 对话式软件修复框架 |
| ConDefects: A Complementary Dataset to Address the Data Leakage Concern | FSE 2024 | 数据泄漏感知修复 |
| ContractTinker: LLM-Empowered Vulnerability Repair for Smart Contracts | ASE 2024 | 智能合约漏洞修复 |

---

### 方向8: 运维智能化 (AIOps) ⭐⭐⭐

**推荐指数**: ★★★☆☆ | **创新空间**: 中高 | **工业需求**: 大

**关键论文**:
| 论文 | 会议 | 核心贡献 |
|------|------|----------|
| The Potential of One-Shot Failure Root Cause Analysis: Collaboration of LLM and Small Classifier | ASE 2024 | 小分类器+LLM根因分析 |
| FAIL: Analyzing Software Failures from the News Using LLMs | ASE 2024 | 新闻分析软件故障 |
| Exploring LLM-based Agents for Root Cause Analysis | FSE 2024 | LLM Agent根因分析 |
| Automated Root Causing of Cloud Incidents using In-Context Learning with GPT-4 | FSE 2024 | GPT-4云事故根因分析 |
| Face It Yourselves: An LLM-Based Two-Stage Strategy to Localize Configuration Errors via Logs | ISSTA 2024 | 日志配置错误定位 |

---

## 三、科研课题推荐

### 🥇 强烈推荐课题 (新兴方向，创新空间大)

#### 课题A: Multi-Agent协作框架在软件工程任务中的应用

**研究问题**:
- 如何设计一个多LLM Agent协作框架来完成完整的软件开发任务？
- Agent之间如何分解任务、共享信息、协调决策？
- 如何保证多Agent协作的正确性和效率？

**创新点**:
- 首次系统性地将Multi-Agent协作应用于完整软件开发流程
- 设计Agent间的通信协议和任务分解机制
- 在真实软件开发任务上评估框架效果

**可行性**:
- 高：已有基础（Unity Is Strength, Self-collaboration Code Generation）
- 可在现有框架基础上扩展
- 数据和评估指标相对明确

---

#### 课题B: Vibe Coding质量评估框架

**研究问题**:
- 如何系统性地评估Vibe Coding（自然语言编程）生成的代码质量？
- 不同自然语言描述风格如何影响生成代码的质量？
- 如何帮助开发者有效纠错和反馈？

**创新点**:
- 首次提出Vibe Coding质量评估的系统性框架
- 多维度评估指标（功能正确性、可读性、安全性、性能）
- 开发者-Vibe Coding交互反馈机制

**可行性**:
- 高：与你兴趣相关，研究问题清晰
- 可使用现有Vibe Coding系统（如ChatGPT、Copilot）作为实验对象
- 评估指标可定义

---

### 🥈 次推荐课题 (较成熟方向，可做细分创新)

#### 课题C: LLM Agent安全对抗研究

**研究问题**:
- 如何攻击LLM Agent在软件工程任务中的行为？
- 如何防御这些攻击？
- 多Agent系统中的安全信任边界如何定义？

**创新点**:
- 从对抗角度研究LLM Agent
- 提出针对软件工程任务的对抗攻击方法
- 设计防御机制

---

#### 课题D: 多粒度程序修复

**研究问题**:
- 如何在不同粒度（语句、函数、模块）上生成修复补丁？
- 如何选择最合适的修复粒度？
- 多粒度修复如何提升修复效果？

**创新点**:
- 继承One Size Does Not Fit All的思路，但更进一步
- 提出自适应多粒度选择机制
- 在更大规模的bug数据集上评估

---

## 四、CCF-A会议信息速查

| 会议 | 全称 | CCF级别 | 2024论文总数 | LLM相关论文数 | 论文优先级 |
|------|------|---------|-------------|---------------|------------|
| ICSE | International Conference on Software Engineering | A | ~180 | ~30 | 极高 |
| FSE | ACM SIGSOFT International Symposium on Software Engineering | A | ~120 | ~20 | 极高 |
| ASE | IEEE/ACM International Conference on Automated Software Engineering | A | ~150 | ~30 | 高 |
| ISSTA | International Symposium on Software Testing and Analysis | A | ~80 | ~15 | 高 |
| OOPSLA | ACM SIGPLAN Conference on Object-Oriented Programming | A | ~120 | ~15 | 中高 |

---

## 五、下一步行动建议

### 立即行动（本周）
1. **精读关键论文**: 选择2-3篇上述论文深入阅读，理解研究范式
2. **确定研究兴趣**: 在Multi-Agent协作 vs Vibe Coding评估之间做出选择
3. **复现基线**: 选择一个论文的基线系统进行复现

### 短期目标（本月）
1. **确定研究课题**: 完成开题报告初稿
2. **获取实验数据**: 收集或选择合适的代码数据集
3. **设计实验方案**: 明确评估指标和实验方法

### 中期目标（下学期）
1. **实现原型系统**: 完成系统设计和实现
2. **实验验证**: 在多个数据集上验证效果
3. **论文写作**: 撰写并投稿CCF-A会议

---

## 六、关键论文清单 (可直接搜索)

### Multi-Agent相关
- Unity Is Strength: Collaborative LLM-Based Agents for Code Reviewer Recommendation (ASE 2024)
- Can Cooperative Multi-Agent Reinforcement Learning Boost Automatic Web Testing? (ASE 2024)
- Self-collaboration Code Generation via ChatGPT (ASE 2024)
- Exploring LLM-based Agents for Root Cause Analysis (FSE 2024)

### Vibe Coding相关
- PlayCoder: Making LLM-Generated GUI Code Playable (ASE/arXiv)
- Self-Elicitation of Requirements with Automated GUI Prototyping (ASE 2024)
- Getting Inspiration for Feature Elicitation: App Store- vs. LLM-based Approach (ASE 2024)

### 测试生成相关
- Towards Understanding the Effectiveness of Large Language Models on Directed Test Input Generation (ASE 2024) ⭐ Distinguished Paper
- Evaluating and Improving ChatGPT for Unit Test Generation (FSE 2024)
- UniTSyn: Large-Scale Dataset for Enhancing LLM for Program Testing (ISSTA 2024)

### AI Chain/Workflow相关
- Prompt Sapper: A LLM-Empowered Production Tool for Building AI Chains (ASE 2024)
- LLM4Workflow: An LLM-based Automated Workflow Model Generation Tool (ASE 2024)

### 安全相关
- Imperceptible Content Poisoning in LLM-Powered Applications (ASE 2024)
- Attacking and Defending Large Language Models on Coding Tasks (ASE 2024)
- CoSec: On-the-Fly Security Hardening of Code LLMs (ISSTA 2024)

---

*报告生成时间: 2026-04-22*
*数据来源: ASE 2024官网, FSE 2024官网, ISSTA 2024论文列表*
