---
title: Program Repair (LLM辅助程序修复)
created: 2026-04-22
updated: 2026-04-22
type: concept
tags: [program-repair, CCF-A, LLM, research-trend]
sources: [ASE-2024, ISSTA-2024]
---

## 定义

LLM辅助程序修复(Automated Program Repair, APR)指利用大语言模型自动检测和修复软件bug的技术方向。这是软件工程领域的经典问题，LLM为其带来了新的突破。

## 研究现状

### 核心论文

| 论文 | 会议 | 亮点 |
|------|------|------|
| One Size Does Not Fit All: Multi-granularity Patch Generation ⭐ | ISSTA 2024 | **Distinguished Paper** - 多粒度补丁生成 |
| ContractTinker: LLM-Empowered Vulnerability Repair for Smart Contracts | ASE 2024 | 智能合约漏洞修复 |
| CREF: An LLM-Based Conversational Software Repair Framework for Programming Tutors | ISSTA 2024 | 会话式程序修复教学 |
| Neurosymbolic Repair of Test Flakiness | ISSTA 2024 | 神经符号化修复Flaky Test |

### 修复粒度

1. **Statement-level (语句级)**: 修改单行代码
2. **Method-level (方法级)**: 修改整个方法/函数
3. **File-level (文件级)**: 修改整个文件或多个文件

## 核心问题

- LLM能否修复真实复杂bug？
- 多粒度补丁如何选择和评估？
- 如何避免"看起来对但实际错"的修复（正确性保证）？
- 修复的可解释性和可审查性？

## 相关方向

- [[test-generation]] — 测试生成可用于验证修复正确性
- [[llm-security]] — 安全漏洞修复是重要子方向
- [[code-quality-assessment]] — 修复质量评估是核心问题
