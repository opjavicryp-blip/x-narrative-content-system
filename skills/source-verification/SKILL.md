# Source Verification Skill

## Purpose

Decide what can be stated as fact, what must be attributed, what must be softened, and what cannot be published yet.

Research finds leads. Verification establishes claims.

## When to Load

Load when a claim, chart, screenshot, quote, calculation, or causal explanation may be used in output.

Do not load merely to brainstorm or collect headlines.

## Evidence Hierarchy

### Tier 1 - Primary

- Official filings, issuer data, prospectuses, company releases
- Central-bank statements and transcripts
- Government data: BLS, BEA, Treasury, FRED, SEC, CFTC
- Exchange or fund administrator data
- Direct blockchain transaction, block height, UTXO ancestry, explorer link

### Tier 2 - Reported primary evidence

- Reputable reporting that directly cites and links to Tier 1 material

### Tier 3 - Leads and specialist analysis

- Research providers, on-chain dashboards, analysts, newsletters
- Accept only with disclosed methodology and, where possible, cross-checking

### Tier 4 - Unverified leads

- Screenshots, social posts, anonymous claims, cropped charts, unattributed images

Tier 4 never proves a claim.

## Mandatory Claim Ledger

Every publication-bound claim must be entered before writing.

| Field | Requirement |
|---|---|
| Claim | Exact sentence proposed for publication |
| Type | Fact / calculation / quote / paraphrase / interpretation / causal claim |
| Evidence | Direct source or source chain |
| Source tier | 1-4 |
| Data timestamp | Date and time, if relevant |
| Freshness | CURRENT or CONTEXT |
| Calculation | Formula, inputs, and result if derived |
| What it does not prove | Explicit limitation |
| Contradictory evidence | What conflicts or complicates it |
| Status | Verified / Partially verified / Unverified / Blocked |

## Required Checks

### 1. Provenance

- Find the original document, filing, transcript, dashboard, or transaction.
- A screenshot is insufficient without the underlying source.
- A chart requires source, date, unit, cohort definition, and methodology.

### 2. Quote Check

- Quotation marks require verbatim wording and a direct source.
- If wording is paraphrased, remove quotation marks and say it is a paraphrase.
- Do not attribute a paraphrase to a named speaker as a quote.

### 3. Timestamp Check

- Recheck every time-sensitive number immediately before drafting.
- State the date where an older number could be mistaken for current.
- Replace superseded values with the latest verifiable value.

### 4. Calculation Check

- Show the formula.
- Use signed values correctly.
- Verify the time interval.

Example:
`-$201M on Sep 1 to +$454M on Sep 3 = $655M directional swing over two trading days.`

It is not a $407M move and not one session.

### 5. Claim-Scope Check

Do not collapse distinct claims:
- Building a product is not launching a product.
- Offering access is not customer adoption.
- ETF flow is not automatically spot buying or selling at that moment.
- A 50 BTC movement is not automatically a 2010 coinbase reward.
- A Satoshi-era coin is not evidence of Satoshi ownership.
- A moved coin is not evidence of sale intent.

### 6. Causality Check

Use causal language only when direct evidence supports it.

Prefer:
- "coincided with"
- "followed"
- "is consistent with"
- "may have contributed"

Avoid:
- "drove"
- "caused"
- "proves"

unless the causal link is actually established.

### 7. Contradiction Check

Ask:
1. What supports the claim?
2. What contradicts or complicates it?
3. What newer disclosure could supersede it?
4. What would falsify the interpretation?

## Publication Status

### VERIFIED
Primary evidence supports the exact claim, timing, calculation, and scope.

### PARTIALLY VERIFIED
A narrower claim is supported, but wording must be attributed or softened.

### UNVERIFIED
Evidence is incomplete, indirect, or conflicting. Do not present as fact.

### BLOCKED
A necessary primary source, transaction identifier, methodology, calculation, or direct quote cannot be established. Do not publish the claim.

## Required Output

```markdown
## Verification: [Topic]
## Timestamp: [UTC/local]

### Claim Ledger
| Claim | Type | Tier | Timestamp | Status | Caveat |
|---|---|---:|---|---|---|

### Contradiction Check
- Supporting evidence:
- Complicating evidence:
- More recent data checked:
- What would change the conclusion:

### Publish-Safe Language
- [Approved wording]

### Blocked Language
- [Wording that must not be used]
```

## Interfaces

### Input
- Deep-research evidence pack
- Candidate claims, charts, quotes, and calculations

### Output
- Claim ledger
- Publication-safe wording
- Contradiction summary
- Verification status

### Passes To
- narrative-analysis only when required claims are verified or safely qualified
- x-writing only with publication-safe wording

---

*Skill version: 3.0 | Last updated: 2026-09-06*