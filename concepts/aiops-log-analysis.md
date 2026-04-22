---
title: AIOps & Log Analysis (LLM辅助运维与日志分析)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [aiops, CCF-A, LLM, log-analysis, research-trend]
sources: [ASE-2024, ISSTA-2024]
---

## 定义

AIOps & Log Analysis研究利用大语言模型辅助运维、进行日志分析、故障定位、根因分析等任务。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| Face It Yourselves: An LLM-Based Two-Stage Strategy to Localize Configuration Errors via Logs | ISSTA 2024 | 日志配置错误定位 |
| FAIL: Analyzing Software Failures from the News Using LLMs | ASE 2024 | 新闻分析软件故障 |
| The Potential of One-Shot Failure Root Cause Analysis: Collaboration of LLM and Small Classifier | ASE 2024 | 小分类器+LLM协作根因分析 |
| Predictive Autoscaling for Node.js on Kubernetes | ASE 2024 | K8s智能扩缩容 |

## 核心问题

- LLM能否理解海量日志并进行根因分析？
- 如何结合传统ML和LLM做运维智能化？
- 实时性和准确性的平衡？

## 相关方向

- [[workflow-automation]] — 智能运维可整合入工作流
- [[program-comprehension]] — 日志理解依赖程序理解能力
- [[multi-agent-collaboration]] — 多Agent可用于复杂故障诊断
