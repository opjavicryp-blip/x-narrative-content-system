# Market Research Skill

## Purpose

Find fresh events (last 24h), gather market data, identify unusual movements, form initial thesis.

## When to Load

Load this skill when task requires:
- ✅ Finding what happened in last 24 hours
- ✅ Gathering BTC, equities, macro, or flow data
- ✅ Identifying unusual market movements
- ✅ Forming initial thesis from data

Do NOT load when:
- ❌ Validating a claim (use source-verification)
- ❌ Connecting to narrative (use narrative-analysis)
- ❌ Writing content (use x-writing)

## Evidence Window

**Default: CURRENT (last 24 hours)**

Examples:
- ETF flows: yesterday's data only
- Price action: today's move
- News: last 24h events
- Fed statements: most recent commentary

**Exception: CONTEXT (label explicitly)**

Examples:
- Historical patterns: "In 2020-2024, ETF inflows led by 1-3 days"
- Structural relationships: "M2 growth typically precedes BTC rallies"
- Background: "GBTC has been outflowing since January"

## Data Sources

### Tier 1 (Primary)

| Data Type | Source | Tool |
|-----------|--------|------|
| ETF Flows | Fidelity IBIT, Grayscale GBTC, BlackRock | finance_etf_holdings |
| Institutional Holdings | SEC 13F filings | finance_institutional_holders |
| Insider Trades | SEC Form 4 | finance_insider_transactions |
| Macro Data | FRED, BLS, BEA | finance_macro_snapshot, finance_macro_history |
| Earnings | Company filings | finance_earnings_history, finance_earnings_schedule |
| Price History | Exchange data | finance_ohlcv_histories |

### Tier 2 (Aggregated)

| Data Type | Source | Tool |
|-----------|--------|------|
| Analyst Estimates | Consensus data | finance_estimates |
| Company Profile | Business description | finance_company_profile |
| Peers | Comparable companies | finance_company_peers |
| Segments | Revenue by segment | finance_segments |

## Workflow

### Step 1: Define Research Question

Be specific about time window:

```
Good: "What drove BTC price action in last 24h?"
Good: "What are this week's ETF flow trends?"
Bad: "What's happening with Bitcoin?" (too vague)
```

### Step 2: Gather Current Evidence (24h)

Query for each relevant data type:

```
1. ETF Flows
   - IBIT, FBTC, GBTC daily flows
   - Total industry net flow
   - Any unusual single-day moves

2. Price Action
   - BTC, ETH major crypto
   - Key equities (COIN, MSTR, miners)
   - Related ETFs

3. Macro Catalysts
   - Fed speakers in last 24h
   - Economic data releases (CPI, NFP, PCE)
   - Yield curve moves
   - DXY, liquidity metrics

4. Unusual Movements
   - Volume spikes (>2x average)
   - Price gaps (>5% moves)
   - Options flow (if available)
   - Whale transactions (on-chain)
```

### Step 3: Form Initial Thesis

Structure:

```
## Current Evidence (Last 24h)

### Key Data Points
- [Data point 1] - [Source] - [Timestamp]
- [Data point 2] - [Source] - [Timestamp]

### Unusual Movements
- [What stood out vs. normal patterns]

### Initial Thesis
[1-2 sentences explaining what's driving action]

### Evidence Classification
- CURRENT: [List items from last 24h]
- CONTEXT: [List any historical/background used]
```

### Step 4: Flag for Verification

Before passing to next skill:

```
## Verification Flags

### Claims Needing Source-Verification
- [Claim 1]: Needs confirmation from [primary source]
- [Claim 2]: Timestamp unclear, verify [source]

### Contradictions to Check
- [Data point A] seems to contradict [Data point B]
- [Social media claim] conflicts with [official data]

### Gaps
- [What data is missing for complete picture]
```

## Output Format

```markdown
## Research: [Topic]
## Date: [YYYY-MM-DD]
## Evidence Window: CURRENT (last 24h) + CONTEXT (labeled)

### Current Evidence

#### ETF Flows
- IBIT: +$180M (2026-09-04) [finance_etf_holdings]
- GBTC: -$50M (2026-09-04) [finance_etf_holdings]
- Total: +$130M net [calculated]

#### Price Action
- BTC: +3.2% to $58,400 (24h) [finance_ohlcv_histories]
- COIN: +5.1% [finance_quotes]
- MSTR: +4.8% [finance_quotes]

#### Macro
- No Fed speakers in last 24h
- 10Y yield: -8bps to 4.12% [finance_macro_snapshot]
- DXY: -0.4% [finance_quotes]

#### Unusual Movements
- BTC volume 2.3x 30-day average
- IBIT largest inflow since 2026-08-28

### Contextual Evidence (Labeled)

- GBTC has been outflowing since January 2026 [CONTEXT]
- M2 growth turned positive in July 2026 [CONTEXT]
- Historical pattern: ETF inflows lead price by 1-3 days [CONTEXT]

### Initial Thesis

BTC rally driven by combination of ETF rotation (GBTC → IBIT/FBTC) and macro liquidity improvement (falling yields, weaker DXY). Volume surge suggests institutional participation.

### Verification Flags

#### Claims Needing Source-Verification
- "Volume 2.3x average": Verify against 30-day calc
- "Largest inflow since 2026-08-28": Check exact date

#### Contradictions to Check
- None identified

#### Gaps
- On-chain whale data not checked
- Options flow not available

### Confidence: Medium

Reason: ETF and price data verified. Volume claim needs confirmation. On-chain data missing.
```

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Using old data without labeling | Mark as [CONTEXT] or find current data |
| Vague research question | Specify time window and data types |
| Mixing CURRENT and CONTEXT | Separate sections clearly |
| Skipping verification flags | Always flag claims needing check |
| Overcomplicating thesis | 1-2 sentences, data-driven |

## Interfaces

### Input
- Research question with time window
- List of data types to gather

### Output
- Current evidence (last 24h)
- Contextual evidence (labeled)
- Initial thesis
- Verification flags
- Confidence level

### Passes To
- **source-verification**: For claim validation
- **narrative-analysis**: For thesis connection to narrative
- **x-writing**: If immediate publish needed (skip narrative)

---

*Skill version: 2.0 | Last updated: 2026-09-05*
