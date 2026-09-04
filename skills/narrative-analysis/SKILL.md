# Narrative Analysis Skill

## Purpose

Determine what this account should say next. Connect new information to previous theses. Identify gaps, contradictions, and narrative momentum.

## When to Load

Load this skill when:
- ✅ Determining what to post next based on research
- ✅ Connecting new info to account's previous content
- ✅ Identifying narrative gaps or contradictions
- ✅ Tracking which narratives are gaining/losing momentum
- ✅ Finding contrarian angles

Do NOT load when:
- ❌ Gathering fresh data (use market-research)
- ❌ Validating claims (use source-verification)
- ❌ Pure expression/writing (use x-writing)

## Evidence Window

**NARRATIVE: No time restriction**

This skill uses:
- Account's previous posts (any time)
- Past theses and conclusions
- Narrative-state.md (current narrative map)
- Account-positioning.md (who we are)

**CURRENT: Only when checking narrative momentum**

Examples:
- "Is ETF flow narrative still dominant?" → Check last 24h mentions
- "Did macro narrative gain traction this week?" → Check last 7d

## Inputs

### Required
- Verified claims from source-verification **OR**
- Research output from market-research (with verification flags resolved)

### Load These References
- narrative-state.md (current narrative map)
- account-positioning.md (who we are, what we cover)

## Workflow

### Step 1: Review Verified Information

From source-verification output:

```
Verified Claims:
- IBIT +2,847 BTC on 2026-09-04 ✅
- ETF inflows one of several drivers (not sole driver) ✅
- Macro liquidity improving (yields down, DXY down) ✅
```

### Step 2: Check Narrative-State.md

What narratives are currently tracked?

```
From narrative-state.md:

Bitcoin Narrative (as of 2026-09-05):
- Consensus: ETF flows dominant driver
- Competing: Macro liquidity, technicals, miner dynamics
- Contrarian angle: ETF flows are lagging, macro leads
```

### Step 3: Check Account's Previous Posts

What has this account said recently?

```
Search account's X posts (last 14 days):
- 2026-08-28: "GBTC rotation to IBIT continuing. Outflows slowing but still dominant theme."
- 2026-09-01: "M2 growth turned positive. This matters more than ETF flows over 2-4 week window."
- 2026-09-03: "Real yields peaked. Liquidity setup improving for risk assets."
```

### Step 4: Identify Narrative Position

Ask:

```
1. Does this new information advance existing thesis?
   - Yes: M2 + real yields align with Sep 1 liquidity thesis
   
2. Does it contradict anything previously said?
   - No: Consistent with "macro leads, ETFs lag" view
   
3. What's the logical next post?
   - Connect today's ETF data to macro framework
   - Show how both fit the liquidity thesis
   
4. What narrative gap does this fill?
   - Market focused on ETFs only
   - Gap: Explain why macro matters more over 2-4 weeks
   
5. What's the contrarian angle?
   - Consensus: "ETFs driving rally"
   - Contrarian: "ETFs are noise, macro liquidity is signal"
```

### Step 5: Assess Narrative Momentum

Is the narrative gaining or losing traction?

```
Narrative: "Macro liquidity drives BTC"

Evidence of momentum:
- M2 growth positive (new data)
- Real yields peaked (new data)
- DXY weakening (new data)
- Fed speakers turning less hawkish (check last 48h)

Momentum: GAINING

Narrative: "ETF flows drive BTC"

Evidence:
- IBIT inflows strong (confirmed)
- But price correlation weakening (check 7d correlation)
- Media headlines still ETF-focused (check last 24h news)

Momentum: STABLE (but may be peaking)
```

### Step 6: Form Narrative Thesis

Structure:

```
## Narrative Analysis: [Topic]
## Date: [YYYY-MM-DD]

### Verified Information
[List claims from source-verification]

### Narrative Context
[What account has said before on this topic]

### Narrative Position
- Advances thesis: [How this connects]
- Contradictions: [Any conflicts with past posts]
- Gaps filled: [What this explains]

### Contrarian Angle
[How this differs from consensus narrative]

### Recommended Next Content
[What to post, why it matters now]

### Confidence
[High/Medium/Low based on evidence strength]
```

## Output Format

```markdown
## Narrative Analysis: BTC Rally Drivers
## Date: 2026-09-05

### Verified Information

- IBIT +2,847 BTC (+$180M) on 2026-09-04 ✅
- ETF inflows are one of several drivers, not sole driver ✅
- Macro liquidity improving: 10Y yield -8bps, DXY -0.4% ✅
- M2 growth turned positive in July 2026 ✅
- Real yields peaked in late July 2026 ✅

### Narrative Context

**Account's Previous Posts:**
- 2026-08-28: "GBTC rotation to IBIT continuing. Outflows slowing but still dominant theme."
- 2026-09-01: "M2 growth turned positive. This matters more than ETF flows over 2-4 week window."
- 2026-09-03: "Real yields peaked. Liquidity setup improving for risk assets."

**Current Narrative Map (narrative-state.md):**
- Consensus: ETF flows dominant driver
- Contrarian angle: ETF flows are lagging, macro liquidity leads by 2-4 weeks

### Narrative Position

**Advances Thesis:**
- Today's ETF data fits the "ETFs are noise, macro is signal" framework
- M2 + real yields data from Sep 1 thesis playing out as expected
- Strengthens contrarian position vs. ETF-only narrative

**Contradictions:**
- None identified. Consistent with all recent posts.

**Gaps Filled:**
- Market focused on ETF flows as sole driver
- This connects ETF data to macro framework
- Explains why rally has broader support than consensus thinks

### Contrarian Angle

**Consensus:** "ETF inflows driving BTC rally"

**Contrarian View:** ETF flows are coincident, not causal. Macro liquidity (M2, real yields, DXY) leads by 2-4 weeks. Today's ETF data is noise within that larger signal.

**Evidence:**
- M2 growth turned positive in July (leads by 4-8 weeks historically)
- Real yields peaked late July (leads by 2-4 weeks)
- ETF flows correlate but don't lead (check 30d correlation)

### Recommended Next Content

**Post Type:** Contrarian take + data

**Thesis:** "Everyone's watching ETF flows. They're looking at the wrong metric."

**Supporting Data:**
- IBIT +$180M yesterday (acknowledge consensus view)
- M2 +0.3% in July, first positive in 18 months (key metric)
- Real yields peaked at 2.1% in late July, now 1.9% (liquidity improving)

**Narrative Connection:**
- Continues Sep 1 liquidity thesis
- Provides fresh data point (yesterday's flows)
- Contrarian angle: ETFs are lagging indicator

**Confidence:** High

**Reason:**
- All claims verified against primary sources
- Consistent with account's previous theses
- Contrarian angle supported by historical patterns
- No contradictory evidence found

### What NOT to Post

❌ "ETFs are the only driver" (oversimplifies, contradicts verified data)
❌ "Macro doesn't matter, only ETFs" (false dichotomy, easily debunked)
❌ "BTC to $100K next week" (price target without evidence)
```

## Interfaces

### Input
- Verified claims from source-verification
- Research output (optional, if verification not needed)
- Access to account's previous posts (X history)

### Output
- Narrative position (advances/contradicts/fills gaps)
- Contrarian angle
- Recommended next content
- Confidence level
- What NOT to post

### Passes To
- **x-writing**: For expression of recommended content
- **market-research**: If gaps identified, need more data
- **source-verification**: If new claims need checking before publishing

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Forcing narrative continuity | Only connect if genuine link exists |
| Ignoring account's previous posts | Always check what's been said before |
| Overcomplicating contrarian angle | Keep it simple, data-backed |
| Not assessing momentum | Check if narrative gaining/losing traction |
| Confusing narrative with truth | Narrative explains, doesn't create, reality |

---

*Skill version: 2.0 | Last updated: 2026-09-05*
