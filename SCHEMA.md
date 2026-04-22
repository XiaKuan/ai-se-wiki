# Wiki Schema

## Domain
LLM Agent × Software Engineering CCF-A Conference Research
覆盖：大语言模型Agent在软件工程CCF-A会议（ICSE、FSE、ASE、ISSTA、OOPSLA）中的最新研究趋势、课题方向和论文调研。

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `multi-agent-collaboration.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- 主要内容使用中文，专业词汇和标题使用英文

## Frontmatter
```yaml
---
title: Page Title
created: 2026-04-22
updated: 2026-04-22
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
---
```

## Tag Taxonomy
- **研究方向**: test-generation, program-repair, multi-agent, security, formal-verification, ui-automation, aiops, workflow-automation, code-review, vibe-coding, requirements, program-comprehension
- **会议级别**: CCF-A, ICSE, FSE, ASE, ISSTA, OOPSLA
- **模型技术**: LLM, code-llm, prompt-engineering, RAG, fine-tuning
- **评估方法**: benchmark, evaluation, empirical-study
- **Meta**: research-trend, literature-review, gap-analysis

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions, minor details, or things outside the domain
- **Split a page** when it exceeds ~200 lines — break into sub-topics with cross-links

## Update Policy
When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Flag for user review

## Wiki Link Rules
Every page must link to at least 2 other pages via [[wikilinks]].
