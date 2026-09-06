# Market Research Skill

## Purpose

Surface current research opportunities. This skill is a scanner first, not a thesis factory.

It finds timely topics, gathers enough evidence to rank them, and stops. Deep research begins only after the user selects a topic.

## When to Load

Load when the user asks for:
- Current market scan
- 5-10 content ideas
- Fresh BTC, equities, macro, ETF-flow, or policy developments
- Unusual moves or possible catalysts

Do not load for:
- Claim validation - use source-verification
- Narrative continuity - use narrative-analysis
- Post drafting - use x-writing

## Freshness Rules

### CURRENT
Default window: last 24 hours.

Use for prices, flows, news, statements, filings, on-chain movements, policy actions, and platform changes.

### CONTEXT
No time restriction. Label it explicitly as context.

Use for historical comparisons, recurring patterns, structural mechanisms, and background.

### NARRATIVE
No time restriction.

Use account history only through narrative-analysis, not as a substitute for current evidence.

## Mode A - Topic Scan

### Objective

Return 5-10 candidate topics and rank the three strongest. Do not perform deep research, verification, narrative analysis, or writing until the user chooses a topic.

### Source Order

1. Tier 1: official filings, issuers, central banks, government agencies, exchanges, transcripts, direct blockchain data
2. Tier 2: reputable reporting that links to Tier 1
3. Tier 3: specialist data providers and commentary, only as leads unless methodology is available
4. Tier 4: screenshots, anonymous posts, social claims - leads only

### Scan Procedure

1. Search CURRENT evidence across relevant domains.
2. Produce 5-10 topics, each with one or two source-backed facts.
3. Separate fact from proposed angle.
4. Score every topic from 1 to 5 on:
   - Freshness
   - Source quality
   - Materiality
   - Novelty / non-consensus angle
   - Fit with account positioning
5. Flag the main caveat or contradiction.
6. Rank the three strongest topics.
7. STOP and wait for user selection.

### Required Output

```markdown
## Market Research Scan
## Timestamp: [UTC/local]
## Current Evidence Window: last 24h

| Rank | Topic | Why now | Primary evidence | Caveat | Score |
|---|---|---|---|---|---|

### Top 3

1. [Topic]
   - Verified fact: [fact + source]
   - Why it could matter: [bounded interpretation]
   - Main risk: [what is not known]
   - Suggested deep-research question: [precise question]

### Stop Condition
Select one or more topics for deep research. No draft is produced in scan mode.
```

## Mode B - Deep Research

Run only after the user explicitly chooses a topic.

### Procedure

1. Define a narrow research question and current time window.
2. Gather Tier 1 evidence first.
3. Use Tier 2 only to discover or corroborate evidence, not to replace Tier 1 when Tier 1 exists.
4. Label each item CURRENT or CONTEXT.
5. Create a preliminary claim ledger for source-verification.
6. Identify alternative explanations and missing data.

### Required Output

```markdown
## Research: [Topic]
## Timestamp: [UTC/local]
## Evidence Window: CURRENT + labeled CONTEXT

### Current Evidence
- [Fact] | [source] | [timestamp]

### Context
- [Historical/background fact] | [source] | [date]

### Initial Thesis
[One bounded, falsifiable interpretation.]

### Alternative Explanations
- [Alternative]

### Verification Queue
- [Exact claim requiring source-verification]

### Gaps
- [Missing data]
```

## Hard Rules

- A screenshot is a lead, not evidence.
- Do not treat a social post, chart, or headline as a primary source.
- Do not claim causation from coincidence.
- Do not call an item "current" if it is older than 24 hours without stating its date.
- Do not turn one source into a market-wide conclusion.
- Stop after the scan unless the user selects a topic.

## Interfaces

### Input
- Scan request or selected topic
- Relevant market / asset universe

### Output
- Mode A: ranked topic shortlist and stop condition
- Mode B: evidence pack, bounded thesis, verification queue

### Passes To
- source-verification after deep research
- narrative-analysis only after claims are verified

---

*Skill version: 3.0 | Last updated: 2026-09-06*