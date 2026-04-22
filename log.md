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

## [2026-04-23] update | AI-Ops/AIware 2025 调研更新
- Sources: AIware 2025 program page, arXiv:2604.19742, 2602.13156, 2602.02585, 2407.04065, 2511.15755
- Topics: AI-Ops科研空白、Autonomous SRE Agent、Multi-Agent Incident Response、运维数据集
- Pages updated: [[aiops-log-analysis]] (重构，新增arXiv高价值论文、AIware论文、研究空白)
- Pages created: [[aiware-2025]] (AIware 2025实体页面，Main Track + Benchmark&Dataset Track论文)
- Key findings:
  - arXiv:2604.19742是首个完整"Deploy-Calibrate-Monitor-Heal"自主SRE Agent
  - arXiv:2407.04065 (LBOps) 是运维数据集研究的直接参考
  - AIware Benchmark & Dataset Track是运维数据集的重要来源
  - 研究空白：运维数据集质量量化评估、Autonomous SRE评测基准
