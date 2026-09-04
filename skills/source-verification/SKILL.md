# Source Verification Skill

## Objective

Validate claims, data, and sources before publishing to maintain credibility and avoid spreading misinformation.

## Verification Protocol

### Tier 1: Primary Sources (Highest Trust)

- **Official filings**: SEC 13F, Form 4, 10-K, 10-Q
- **Government data**: BLS, BEA, Federal Reserve, Treasury
- **Company disclosures**: Earnings releases, investor presentations
- **Exchange data**: CME, NYSE, NASDAQ official data
- **On-chain data**: Direct blockchain explorers (mempool, Etherscan)

### Tier 2: Aggregated Data (High Trust)

- **Financial APIs**: Bloomberg, PitchBook, finance_tickers_lookup
- **Established media**: Reuters, WSJ, FT, Bloomberg News
- **Industry data**: CoinMetrics, Glassnode (for crypto)
- **Academic sources**: NEJM, peer-reviewed journals

### Tier 3: Secondary Commentary (Medium Trust)

- **Analyst reports**: Bank research, independent analysts
- **Newsletters**: Credible Substack authors with track record
- **Social media**: Verified analysts with primary source links

### Tier 4: Unverified Claims (Low Trust)

- **Anonymous X accounts** without source links
- **Reddit/Telegram rumors**
- **Screenshots without context or timestamps**
- **Old articles** presented as current news

## Verification Checklist

### For Data Claims

- [ ] Can I find this number in the original source?
- [ ] Is the timestamp current (not recycled old data)?
- [ ] Does the source have direct access to this data?
- [ ] Are there 2+ independent sources confirming?
- [ ] Is the methodology transparent?

### For Social Media Claims

- [ ] Does the post link to primary source?
- [ ] Is the account verified and credible?
- [ ] What's their track record on this topic?
- [ ] Are replies calling out errors?
- [ ] Can I independently verify the claim?

### For Charts/Screenshots

- [ ] Is the source visible in the screenshot?
- [ ] Is the timestamp current and legible?
- [ ] Can I recreate this chart from raw data?
- [ ] Are axes/labels clear and not misleading?
- [ ] Is the scale appropriate (no cherry-picked ranges)?

## Red Flags

🚩 **Immediate skepticism required:**

- "Breaking" news from unknown accounts
- Perfect round numbers without context
- Charts with no axis labels or timestamps
- Claims that perfectly fit a narrative
- Screenshots of DMs or private conversations
- "Sources say" without naming sources
- Old headlines shared without date context

## Verification Workflow

### Step 1: Identify the Claim

Extract specific assertions:
- "Bitcoin ETFs had $500M inflows yesterday"
- "Fed is pausing hikes until Q2 2026"
- "Insider selling at [Company] hit record high"

### Step 2: Trace to Source

Find original source:
- Click through link chains
- Search for the exact phrase + date
- Check if multiple outlets report same thing
- Look for primary data (not commentary)

### Step 3: Validate the Data

Cross-check:
- Compare against official data sources
- Check timestamps match claimed timeframe
- Verify methodology (how was this calculated?)
- Look for revisions or corrections

### Step 4: Assess Credibility

Evaluate source:
- What's their track record?
- Do they correct errors publicly?
- Are they transparent about methodology?
- Do they have conflicts of interest?

### Step 5: Document

Record verification:
- Source URL and timestamp
- Verification method used
- Confidence level (high/medium/low)
- Any caveats or limitations

## Source Registry

Maintain a living document (`references/source-registry.md`) with:

```
## Trusted Sources

### ETF Flows
- Fidelity IBIT factsheet (daily)
- Grayscale GBTC holdings page
- Bloomberg ETF flow data

### Macro Data
- Federal Reserve FRED database
- BLS CPI reports
- CME FedWatch Tool

### Crypto On-Chain
- Glassnode (institutional flows)
- CryptoQuant (exchange reserves)
- Mempool.space (miner data)

### Analyst Commentary
- [List of credible X accounts with track record]
- [Newsletters with consistent accuracy]
```

## Common Verification Errors

- **Recency illusion**: Old data presented as new
- **Source drift**: Claim evolves as it's shared, losing accuracy
- **Screenshot deception**: Cropped axes, misleading scales
- **Correlation ≠ causation**: Two things moving together ≠ one causes the other
- **Survivorship bias**: Only showing winners, not losers

## Tools

| Tool | Use Case |
|------|----------|
| Finance API | Verify ETF flows, holdings, insider trades |
| PitchBook/Cashmere | Cross-check private market claims |
| SEC EDGAR | Verify filings directly |
| FRED | Macro data verification |
| Blockchain explorers | On-chain data verification |

## Confidence Levels

When publishing, indicate confidence:

- **High**: Verified against primary source, 2+ confirmations
- **Medium**: Single credible source, plausible but not independently verified
- **Low**: Unverified claim, presenting as "reports say" or "market chatter"

---

*Skill version: 1.0 | Last updated: 2026-09-05*
