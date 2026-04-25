---
title: arXiv AI-Ops 关键论文 (2024-2026)
created: 2026-04-26
updated: 2026-04-26
type: entity
tags: [arXiv, aiops, llm-agent, SRE, autonomous-operations, benchmark]
sources: [arXiv API]
---

## 核心AI-Ops arXiv论文

### 1. ES Guardian Agent — 全生命周期SRE Agent

**Deploy, Calibrate, Monitor, Heal -- No Human Required: An Autonomous AI SRE Agent for Elasticsearch**

| 属性 | 内容 |
|------|------|
| **arXiv ID** | 2604.03933 |
| **方向** | Autonomous SRE Agent |
| **核心贡献** | 11阶段自主SRE: Evaluate→Optimize→Deploy→Calibrate→Stabilize→Alert→Predict→Heal→Learn→Upgrade |
| **关键创新** | 多源预测故障引擎：metrics + logs + kernel级遥测(dmesg/NVMe SMART/NIC bond/thermal) |
| **评估** | 300次自主修复循环、18小时跨系统故障恢复、生产环境验证 |
| **论文特点** | 最完整的AI SRE生命周期论文，接近工业实践 |
| **投稿** | 2026-04-05，FSE 2026投稿 |

### 2. Flow-of-Action — SOP增强多Agent RCA

**Flow-of-Action: SOP Enhanced LLM-Based Multi-Agent System for Root Cause Analysis**

| 属性 | 内容 |
|------|------|
| **arXiv ID** | 2502.08224 |
| **方向** | Multi-Agent RCA |
| **核心贡献** | SOP约束ReAct幻觉，RCA准确率35%→64% |
| **关键创新** | SOP-centric框架：SOP生成→SOP转代码→约束LLM行为 |
| **辅助Agent** | 降噪Agent、空间缩小Agent、停止判断Agent |
| **作者** | Zhe Xie, Zeyan Li, Dan Pei (清华/字节) |

### 3. Network Incident Response Agent

**In-Context Autonomous Network Incident Response: An End-to-End Large Language Model Agent Approach**

| 属性 | 内容 |
|------|------|
| **arXiv ID** | 2602.13156 |
| **方向** | 网络事件响应 |
| **核心贡献** | 端到端LLM Agent网络事件响应 |

### 4. Agentic Observability — 智能告警分类

**Agentic Observability: Automated Alert Triage for Adobe E-Commerce**

| 属性 | 内容 |
|------|------|
| **arXiv ID** | 2602.02585 |
| **方向** | 智能告警分类 |
| **核心贡献** | Adobe电商平台自动化告警分类Multi-Agent |
| **关键创新** | metrics/logs/traces多源数据融合 |

### 5. Multi-Agent Incident Response

**Multi-Agent LLM Orchestration for Incident Response**

| 属性 | 内容 |
|------|------|
| **arXiv ID** | 2511.15755 |
| **方向** | 多智能体事件响应编排 |

### 6. RCAEval Benchmark

**RCAEval: A Benchmark for Root Cause Analysis of Microservice Systems with Telemetry Data**

| 属性 | 内容 |
|------|------|
| **arXiv ID** | 2405.19595 |
| **方向** | RCA Benchmark |
| **核心贡献** | 735故障案例，3个微服务系统，15个baseline |
| **会议** | ISSTA 2024 |
| **特点** | 覆盖粗粒度和细粒度RCA评估 |

### 7. LBOps — 运维工作流研究

**On the Workflows and Smells of Leaderboard Operations (LBOps): An Exploratory Study of Foundation Model Leaderboards**

| 属性 | 内容 |
|------|------|
| **arXiv ID** | 2407.04065 |
| **方向** | DevOps/MLOps运维研究 |
| **核心贡献** | 首个系统性研究基础模型榜单运维问题和工作流 |

## 推荐精读优先级

| 优先级 | 论文 | 理由 |
|--------|------|------|
| ⭐⭐⭐⭐⭐ | ES Guardian Agent (2604.03933) | 最完整SRE Agent，工业验证 |
| ⭐⭐⭐⭐⭐ | Flow-of-Action (2502.08224) | SOP约束多Agent RCA，64%准确率提升 |
| ⭐⭐⭐⭐ | Agentic Memory RCA (ICSE 2026) | 最新进展，Memory增强推理 |
| ⭐⭐⭐⭐ | RCAEval (2405.19595) | 735案例Benchmark |
| ⭐⭐⭐ | Network Incident Response (2602.13156) | 网络运维专项 |

## 相关概念

- [[aiops-log-analysis]] — AIOps日志分析
- [[ICSE-2026]] — ICSE 2026论文
