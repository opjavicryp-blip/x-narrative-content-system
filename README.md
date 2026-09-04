# X Narrative Content System

Modular agent architecture for researching, fact-checking, organizing, and publishing analytical content on X.

## Architecture

```
                    CORE (SKILL.md - Orchestrator)
                     │
                     ▼
                  ROUTER
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
       RESEARCH   NARRATIVE   ALGORITHM
          │          │          │
          └─────┬────┴────┬─────┘
                ▼         ▼
            REFERENCES   SKILLS
                │
                ▼
          CURRENT EVIDENCE
                │
                ▼
       CONTRADICTION CHECK
                │
                ▼
             SYNTHESIS
                │
                ▼
             X-WRITING
                │
                ▼
              OUTPUT
```

## Core Principles

1. **Modularity** - Each skill receives only the context it needs
2. **Freshness** - Current evidence = last 24h; Context = unrestricted but labeled
3. **Verification** - All claims require contradiction check before output
4. **Truth > Narrative** - Don't force connections that don't exist

## Skills

| Skill | Purpose | When to Load |
|-------|---------|-------------|
| [market-research](skills/market-research/SKILL.md) | Find fresh events, gather data, form thesis | When gathering last 24h data |
| [source-verification](skills/source-verification/SKILL.md) | Validate claims, check sources | When claims need verification |
| [narrative-analysis](skills/narrative-analysis/SKILL.md) | Determine what to say next | When connecting to narrative |
| [x-algorithm](skills/x-algorithm/SKILL.md) | X distribution, ranking, engagement | When algorithm questions arise |
| [x-writing](skills/x-writing/SKILL.md) | Express ideas on X | When ready to write/publish |

## References

| Reference | Purpose | Loaded By |
|-----------|---------|-----------|
| [account-positioning.md](references/account-positioning.md) | Who we are, target audience | narrative-analysis, x-writing |
| [writing-style.md](references/writing-style.md) | Voice, tone, formatting | x-writing |
| [narrative-state.md](references/narrative-state.md) | Current narrative map | narrative-analysis |
| [source-registry.md](references/source-registry.md) | Trusted sources | market-research, source-verification |

## Workflow

### Full Pipeline (Research → Publish)

```
1. USER TASK: "What's driving BTC today?"
   ↓
2. ROUTER: Load market-research
   ↓
3. MARKET-RESEARCH: Gather last 24h data (ETF flows, price, macro)
   ↓
4. ROUTER: Load source-verification
   ↓
5. SOURCE-VERIFICATION: Verify claims, check contradictions
   ↓
6. ROUTER: Load narrative-analysis
   ↓
7. NARRATIVE-ANALYSIS: Connect to previous theses, find contrarian angle
   ↓
8. ROUTER: Load x-writing
   ↓
9. X-WRITING: Express as X post
   ↓
10. OUTPUT: Publication-ready post
```

### Partial Pipeline (Answer Question)

```
1. USER TASK: "How does X For You feed work?"
   ↓
2. ROUTER: Load x-algorithm only
   ↓
3. X-ALGORITHM: Check official docs, separate documented vs. inferred
   ↓
4. OUTPUT: Answer with confidence level
```

## Evidence Classification

All evidence must be classified:

### CURRENT (Default: last 24 hours)

- Price action
- ETF flows
- News events
- Fed statements
- Whale movements
- Social media claims

### CONTEXT (No time restriction, must label)

- Historical patterns
- Structural relationships
- Evergreen frameworks
- Background research

### NARRATIVE (No time restriction)

- Account's previous posts
- Past theses and conclusions
- Content continuity

## Token Optimization

### Permanent Context (Always Available)

- SKILL.md (orchestrator)
- All skills (loaded on demand)
- All references (loaded on demand)

### Dynamic Context (Refreshed Per Task)

- Current market data
- Last 24h news
- Current X developments
- Current flows

**Rule:** Never persist dynamic data in permanent context.

## Freshness Rules

```
Current information search = last 24 hours.
Historical/contextual research = unrestricted, but explicitly labeled as context.
```

## Contradiction Check

Before any output, require:

1. What evidence supports this claim?
2. What evidence contradicts or complicates this?
3. What would change my mind?
4. Is there more recent data that supersedes this?

If contradiction check fails → Do not publish. Revise thesis.

## Output Requirements

All outputs must include:

- [ ] Evidence classification (CURRENT/CONTEXT/NARRATIVE)
- [ ] Source citations (from source-registry.md)
- [ ] Contradiction check summary
- [ ] Confidence level (High/Medium/Low)
- [ ] Timestamp of current data

## Usage Examples

### Example 1: Full Research → Publish

**Task:** "What's driving BTC today? Write a post about it."

**Pipeline:**
1. market-research → Gather ETF flows, price, macro (last 24h)
2. source-verification → Verify flow data, check contradictions
3. narrative-analysis → Connect to "macro leads" thesis
4. x-writing → Express as contrarian post

**Output:** Publication-ready post with chart recommendation

### Example 2: Answer Algorithm Question

**Task:** "How does X For You feed ranking work?"

**Pipeline:**
1. x-algorithm → Check xai-org/x-algorithm, X Engineering Blog
2. Separate documented vs. inferred
3. Answer with confidence level

**Output:** Documented ranking signals + community observations (labeled)

### Example 3: Verify Claim

**Task:** "Is it true that BlackRock bought 5,000 BTC yesterday?"

**Pipeline:**
1. source-verification → Check IBIT factsheet, official disclosures
2. Verify exact number, timestamp
3. Classify as fact vs. interpretation

**Output:** Verified/Not Verified status with primary source citation

## Failure Handling

### Insufficient Evidence

```
Status: INSUFFICIENT_EVIDENCE
Reason: [What's missing]
Next Step: [What data needed]
Confidence: Low
```

### Unresolved Contradiction

```
Status: CONTRADICTION_UNRESOLVED
Claim: [What I wanted to say]
Contradiction: [What complicates it]
Resolution: [Revised thesis or defer]
```

### Freshness Ambiguous

```
Status: FRESHNESS_AMBIGUOUS
Claim: [Statement]
Data Age: [When was this from]
Action: [Search for current data or label as context]
```

## Evals

Track quality across four dimensions:

| Eval Type | Purpose | Location |
|-----------|---------|----------|
| [research](evals/research/README.md) | Evaluate research quality | evals/research/ |
| [narrative](evals/narrative/README.md) | Evaluate narrative analysis | evals/narrative/ |
| [writing](evals/writing/README.md) | Evaluate X posts | evals/writing/ |
| [algorithm](evals/algorithm/README.md) | Evaluate post performance | evals/algorithm/ |

## Contributing

This is a living system. Update docs as you learn:

- Add examples from top-performing posts
- Refine checklists based on mistakes
- Update source registry with new discoveries
- Archive evals for pattern recognition

## License

MIT License - Use freely for your own content operations.

---

*System version: 2.0 (Modular Architecture) | Created: 2026-09-05 | Updated: 2026-09-05*
