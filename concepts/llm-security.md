---
title: LLM Security (LLM Agent安全与对抗)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [llm-security, CCF-A, LLM, security, research-trend]
sources: [ASE-2024, ISSTA-2024]
---

## 定义

LLM Agent安全与对抗研究关注大语言模型在软件工程应用中的安全威胁和防御机制，包括对抗样本、数据投毒、恶意代码生成等问题。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| Imperceptible Content Poisoning in LLM-Powered Applications | ASE 2024 | **数据投毒攻击** |
| AdvSCanner: Generating Adversarial Smart Contracts Using LLM + Static Analysis | ASE 2024 | 对抗性智能合约生成 |
| Oracle-Guided Vulnerability Diversity Using LLMs | ASE 2024 | Oracle引导漏洞发现 |
| CoSec: On-the-Fly Security Hardening of Code LLMs via Supervised Co-decoding | ISSTA 2024 | 代码LLM安全加固 |
| Maltracker: NPM Malware Tracker Copiloted by LLM-Enhanced Dataset | ISSTA 2024 | 恶意软件追踪 |
| Evaluating LLM-Generated Obfuscated XSS Payloads | arXiv | 对抗性XSS检测 |

### 研究主题

1. **攻击视角**: 对抗样本、提示注入、数据投毒、恶意代码生成检测
2. **防御视角**: 安全加固、输入过滤、输出检测
3. **红队测试**: LLM安全性的系统化测试方法

## 核心问题

- LLM Agent是否容易被对抗样本欺骗？
- 如何防御LLM生成恶意代码？
- 代码级别的安全如何保证？
- 如何检测LLM生成代码中的安全漏洞？

## 相关方向

- [[program-repair]] — 漏洞修复是安全研究的重要应用
- [[test-generation]] — 安全测试生成是热点方向
- [[workflow-automation]] — AI Chain的安全性考量
