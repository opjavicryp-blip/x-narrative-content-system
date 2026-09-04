# Source Verification Skill

## Purpose

Validate claims, data, and sources. Separate fact from interpretation. Identify contradictions.

## When to Load

Load this skill when:
- ✅ A claim needs validation before publishing
- ✅ Source credibility is unclear
- ✅ Data timestamp is ambiguous
- ✅ Conflicting reports exist
- ✅ Social media claim needs primary source check

Do NOT load when:
- ❌ Gathering fresh data (use market-research)
- ❌ Analyzing narrative position (use narrative-analysis)
- ❌ Writing content (use x-writing)

## Source Tiers

### Tier 1: Primary (Highest Trust)

- **Official filings**: SEC 13F, Form 4, 10-K, 10-Q
- **Government data**: BLS, BEA, Federal Reserve, Treasury
- **Company disclosures**: Earnings releases, investor presentations
- **Exchange data**: CME, NYSE, NASDAQ official data
- **On-chain data**: Direct blockchain explorers

### Tier 2: Aggregated (High Trust)

- **Financial APIs**: Bloomberg, PitchBook, finance_* tools
- **Established media**: Reuters, WSJ, FT, Bloomberg News
- **Industry data**: Glassnode, CryptoQuant (for crypto)

### Tier 3: Commentary (Medium Trust)

- **Analyst reports**: Bank research, independent analysts
- **Newsletters**: Credible Substack authors with track record
- **Social media**: Verified analysts with primary source links

### Tier 4: Unverified (Low Trust)

- Anonymous X accounts without source links
- Reddit/Telegram rumors
- Screenshots without context or timestamps
- Old articles presented as current news

## Verification Protocol

### For Each Claim, Ask:

1. **What is the exact claim?**
   - Extract specific assertion (not vague summary)
   - Example: "BlackRock's IBIT added $180M BTC yesterday" not "ETFs buying"

2. **What is the primary source?**
   - Find original disclosure, filing, or data
   - Not commentary about the source

3. **What is the timestamp?**
   - When was this data from?
   - Is it CURRENT (24h) or CONTEXT (older)?

4. **What exactly was said/reported?**
   - Direct quote or data point
   - Not interpretation or summary

5. **Is this fact or interpretation?**
   - Fact: "IBIT holdings increased by 2,000 BTC"
   - Interpretation: "BlackRock is aggressively accumulating"

6. **What number was reported?**
   - Exact figure, not rounded or approximate
   - Verify calculation if derived

7. **Is there more recent disclosure?**
   - Check if newer data supersedes this
   - Example: Yesterday's flow vs. last week's flow

8. **What contradicts this claim?**
   - Search for opposing evidence
   - Check if other sources disagree

## Verification Workflow

### Step 1: Extract Claims

From research output or user input:

```
Claim: "BlackRock's IBIT added $180M in BTC yesterday"
Claim: "ETF inflows are driving BTC rally"
Claim: "Fed is pausing hikes until Q2 2026"
```

### Step 2: Trace to Source

For each claim:

```
Search: "BlackRock IBIT holdings 2026-09-04"
Search: "IBIT daily flows September 2026"
Search: "Fed speaker [name] [date] statement"
```

Use:
- finance_etf_holdings for ETF data
- finance_earnings_transcript for company statements
- Web search for Fed speakers, news
- SEC EDGAR for filings

### Step 3: Validate Data

```
✓ Primary source found: fidelity.com/etf/factsheet (2026-09-04)
✓ Timestamp matches claim: 2026-09-04
✓ Exact number: +2,847 BTC (+$180M at $58,400)
✓ Classification: CURRENT (within 24h)
```

### Step 4: Assess Credibility

```
Source Tier: Tier 1 (official fund factsheet)
Track Record: No known errors
Transparency: Full holdings disclosed daily
Conflict: None identified
```

### Step 5: Check Contradictions

```
Search: "IBIT outflows September 2026"
Search: "BlackRock reducing BTC position"
Search: "GBTC rotation slowing"

Result: No contradictory data found
```

### Step 6: Classify Evidence

```
[CURRENT] IBIT +2,847 BTC on 2026-09-04 (fidelity.com)
[CONTEXT] IBIT has been largest inflow recipient since launch
[INTERPRETATION] "Aggressive accumulation" - not supported by data (single day)
```

## Output Format

```markdown
## Verification: [Claim or Topic]
## Date: [YYYY-MM-DD]

### Claims Verified

#### Claim 1: "BlackRock's IBIT added $180M in BTC yesterday"

**Status:** ✅ VERIFIED

**Primary Source:**
- URL: fidelity.com/etf/factsheet/ibit
- Date: 2026-09-04
- Data: +2,847 BTC (+$180M)

**Timestamp:** CURRENT (within 24h)

**Fact vs. Interpretation:**
- Fact: +2,847 BTC added ✅
- Interpretation: "Aggressive accumulation" ⚠️ (single day, not trend)

**Contradictions Checked:**
- Searched for outflow reports: None found
- Checked GBTC, FBTC flows: Consistent with rotation narrative

**Confidence:** High

---

#### Claim 2: "ETF inflows are driving BTC rally"

**Status:** ⚠️ PARTIALLY_VERIFIED

**Primary Source:**
- ETF flow data: Verified (fidelity.com, grayscale.com)
- Correlation with price: Needs statistical analysis

**Timestamp:** CURRENT (flows) + CONTEXT (correlation)

**Fact vs. Interpretation:**
- Fact: ETF inflows coincided with rally ✅
- Interpretation: "Driving" implies causation ⚠️ (correlation ≠ causation)

**Contradictions Checked:**
- Macro liquidity also improved (yields down, DXY down)
- On-chain data shows miner selling paused
- Alternative explanation: Macro + technicals, not just ETFs

**Confidence:** Medium

**Note:** Claim oversimplifies. Better: "ETF inflows are one of several drivers alongside macro liquidity improvement."

---

### Summary

| Claim | Status | Confidence | Notes |
|-------|--------|------------|-------|
| IBIT +$180M | ✅ Verified | High | Primary source confirmed |
| ETFs driving rally | ⚠️ Partial | Medium | Correlation verified, causation unclear |

### Recommendations

- ✅ Safe to publish: IBIT flow data
- ⚠️ Reframe before publishing: "ETFs driving" → "ETFs one of several factors"
- ❌ Do not publish: "Aggressive accumulation" (overstates single day)

### Sources Used

- fidelity.com/etf/factsheet/ibit (Tier 1)
- grayscale.com/products/gbtc (Tier 1)
- finance_etf_holdings (Tier 2)
```

## Interfaces

### Input
- Claim(s) to verify
- Research output from market-research (optional)
- Time window for current evidence

### Output
- Verification status per claim
- Primary source citations
- Fact vs. interpretation classification
- Contradiction check results
- Confidence level
- Publish recommendations

### Passes To
- **narrative-analysis**: If verified claims need narrative connection
- **x-writing**: If verified and ready to publish
- **market-research**: If gaps found, need more data

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Accepting commentary as primary source | Find original filing/data |
| Not checking timestamp | Always verify when data is from |
| Confusing fact with interpretation | Separate explicitly |
| Ignoring contradictory evidence | Search for opposing data |
| Overconfidence in partial verification | Use Medium/Low confidence appropriately |

---

*Skill version: 2.0 | Last updated: 2026-09-05*
