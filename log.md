# Wiki Log

> Chronological record of all wiki actions. Append-only.
> Format: `## [YYYY-MM-DD] action | subject`
> Actions: ingest, update, query, lint, create, archive, delete

## [2026-04-22] create | LLM Wiki initialized
- Domain: LLM Agent × Software Engineering CCF-A Conference Research
- Structure created with SCHEMA.md, index.md, log.md

## [2026-04-22] ingest | CCF-A Conference Research Survey
- Sources: ASE 2024, ISSTA 2024 official programs
- Topics covered: 14 research directions, 30+ papers
- Pages created: 15 (14 concepts + 1 comparison + index/log updates)

## [2026-04-22] update | Multi-Agent CCF-A Conference Survey (Round 2)
- Sources: ICSE 2026, ICSE 2025, FSE 2024, FSE 2025 official pages via curl
- Topics: 确认ICSE 2026有4篇multi-agent论文、ICSE 2025有1篇、FSE 2024确认0篇
- Pages updated: [[multi-agent-collaboration]] (重构结构，增加CCF-A逐个检查结果)
- Pages created: [[ICSE-2025]], [[FSE-2024]], [[FSE-2025]]
- Index updated: 15→18 pages
- 待确认: arXiv论文的CCF-A正式发表状态，OOPSLA/SOSP检查

## [2026-04-22] update | Multi-Agent效果评估方法 + 数据集分析
- Sources: arXiv 2511.08475, 2511.18467, 2505.16086, 2512.21818, 2510.03463, 2404.04834 HTML页面
- Topics: 评估方法（4类维度）、数据集（HumanEval/SWE-bench/SRDD）、研究空白
- Pages updated: [[multi-agent-collaboration]] (增加"效果评估方法"和"使用的数据集"两节)
- Key findings: 协作质量评估几乎空白；HumanEval无法评估协作；SRDD是最接近SE的数据集
