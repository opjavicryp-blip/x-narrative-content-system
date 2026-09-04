# X Algorithm Skill

## Purpose

Answer questions about X distribution, ranking, engagement, For You feed, content format, and algorithm changes.

## When to Load

Load this skill when:
- ✅ Question involves X distribution or ranking
- ✅ Engagement optimization needed
- ✅ For You feed behavior questions
- ✅ Content format decisions (thread vs. single post, media, etc.)
- ✅ Algorithm changes or documented behavior

Do NOT load when:
- ❌ Researching market data (use market-research)
- ❌ Validating claims (use source-verification)
- ❌ Analyzing narrative (use narrative-analysis)
- ❌ Pure writing/expression (use x-writing)

## Evidence Window

### CURRENT (Last 24h - 7 days)

- Official announcements from @xai or @XEng
- Notable commits to xai-org/x-algorithm repo
- Documented algorithm changes
- Platform behavior changes users are reporting

### CONTEXT (No time restriction, must label)

- Historical algorithm behavior
- Documented ranking signals (recency, engagement velocity, etc.)
- Evergreen best practices (media richness, reply engagement)
- Research papers or blog posts from X Engineering

## Primary Sources

### Tier 1: Official

| Source | URL | Notes |
|--------|-----|-------|
| X Engineering Blog | blog.x.ai | Official engineering updates |
| xai-org/x-algorithm | github.com/xai-org/x-algorithm | Open-source ranking code |
| @xai (X AI) | twitter.com/xai | Official AI/algorithm announcements |
| @XEng (X Engineering) | twitter.com/XEng | Engineering team updates |
| X Developer Docs | developer.x.com | API and platform documentation |

### Tier 2: Credible Reporting

| Source | Notes |
|--------|-------|
| X official press releases | company.x.com |
| Verified X employees (engineering, product) | Check credentials |
| Reputable tech media (TechCrunch, The Verge) | Cross-reference with official |

### Tier 3: Inference/Community

| Source | Notes |
|--------|-------|
| X creator accounts with testing data | Useful but not official |
| Community observations (X forums, Reddit) | Anecdotal, verify |
| "Algorithm tips" from influencers | Often outdated or wrong |

## Workflow

### Step 1: Identify Question Type

```
Ranking/Distribution:
- "Why did my post get low impressions?"
- "How does For You feed work?"
- "What signals matter for ranking?"

Engagement Optimization:
- "What's the best time to post?"
- "Do threads perform better than single posts?"
- "Should I use images or video?"

Algorithm Changes:
- "Did X change the algorithm this week?"
- "Why is engagement down across the platform?"
- "What's new in the latest update?"

Content Format:
- "Should I post a thread or single tweet?"
- "Do polls help engagement?"
- "How long should my posts be?"
```

### Step 2: Check Official Sources (CURRENT)

```
1. Check xai-org/x-algorithm for recent commits
   - Look for commits in last 7 days
   - Check "Notable Updates" or "Changes" section
   - Note any ranking signal adjustments

2. Check X Engineering Blog
   - Search for posts in last 30 days
   - Look for "ranking", "For You", "algorithm" keywords

3. Check @xai and @XEng
   - Review tweets in last 7 days
   - Look for algorithm or ranking announcements

4. Check X Developer Docs
   - Look for recent API or platform changes
   - Check if any ranking-related endpoints changed
```

### Step 3: Separate Documented vs. Inferred

```
DOCUMENTED (from official sources):
- "For You ranking uses engagement velocity, recency, author authority"
- "Media-rich posts get 2-3x more reach" (X Engineering Blog, 2025-11)
- "First 30 minutes critical for algorithmic testing" (xai-org docs)

INFERRED (from community observation):
- "Posting at 8 AM gets more engagement" (creator testing, not official)
- "Threads with 5-7 tweets perform best" (anecdotal)
- "Replying within 1 hour boosts reach" (community observation)
```

### Step 4: Check for Algorithm Changes

```
Question: "Did X change the algorithm this week?"

Search:
1. xai-org/x-algorithm commits (last 7 days)
2. @xai tweets (last 7 days)
3. @XEng tweets (last 7 days)
4. X Engineering Blog (last 30 days)

If no official changes found:
→ Status: NO_DOCUMENTED_CHANGES
→ Note: Community may be reporting changes, but no official confirmation
→ Recommendation: Monitor engagement patterns, wait for official update
```

### Step 5: Form Answer

Structure:

```
## Algorithm Answer: [Question]
## Date: [YYYY-MM-DD]

### Documented Behavior (Official Sources)
[List what X has officially stated]

### Recent Changes (Last 7 Days)
[Any commits, announcements, or updates]

### Inferred/Community Observations
[What creators are reporting, clearly labeled]

### Recommendation
[Actionable advice based on documented + inferred]

### Confidence
[High/Medium/Low based on source quality]
```

## Output Format

```markdown
## Algorithm: X Ranking Signals
## Date: 2026-09-05

### Question

"What signals does X For You feed use for ranking?"

### Documented Behavior (Official Sources)

**Source:** xai-org/x-algorithm (github.com/xai-org/x-algorithm)
**Last Updated:** 2026-08-28

**Primary Ranking Signals:**

1. **Recency** - Fresh content gets initial boost
   - Decay function: impressions drop ~50% after 2 hours
   - Exception: High-engagement posts can resurface

2. **Engagement Velocity** - Rapid early engagement signals quality
   - Measured: (likes + replies + reposts) / impressions in first 30 min
   - Threshold: >3% engagement rate in first hour = viral potential

3. **Author Authority** - Historical performance on similar topics
   - Topic clustering: X groups authors by content themes
   - Authority score: Based on past engagement on similar topics

4. **Media Richness** - Posts with images/video get 2-3x more reach
   - Source: X Engineering Blog, "Media and Engagement" (2025-11)
   - Video: 3.2x more reach than text-only
   - Images: 2.1x more reach than text-only

5. **Conversation Depth** - Replies and threads increase dwell time
   - Thread engagement: +40% vs. single post (average)
   - Reply engagement: Signals community interest

### Recent Changes (Last 7 Days)

**xai-org/x-algorithm commits:** None in last 7 days
**@xai announcements:** None in last 7 days
**@XEng updates:** None in last 7 days

**Status:** NO_DOCUMENTED_CHANGES

### Inferred/Community Observations

**Not Officially Documented:**

- "Posting at 8-10 AM local time gets more engagement" (creator testing)
- "Replying to comments within 1 hour boosts reach" (community observation)
- "Threads with 5-7 tweets perform best" (anecdotal, varies by topic)

**Note:** These are observations, not confirmed ranking signals.

### Recommendation

**For Maximum For You Reach:**

1. Post fresh content (recency matters)
2. Include visual media (image or video)
3. Engage with replies in first hour (signals conversation)
4. Build authority on specific topics (consistency > variety)
5. Monitor first 30 minutes engagement velocity

**Avoid:**
- Posting without media (2-3x less reach)
- Ignoring replies in first hour (kills conversation signals)
- Inconsistent topic focus (dilutes authority signal)

### Confidence: High

**Reason:** All ranking signals cited from official xai-org/x-algorithm repository and X Engineering Blog. No recent changes to document.

### Sources

- github.com/xai-org/x-algorithm (Tier 1)
- blog.x.ai "Media and Engagement" (2025-11) (Tier 1)
- Community observations (Tier 3, labeled as inferred)
```

## Interfaces

### Input
- Question about X distribution, ranking, engagement, or algorithm
- Time window for current evidence (default: 7 days)

### Output
- Documented behavior (from official sources)
- Recent changes (if any)
- Inferred/community observations (clearly labeled)
- Actionable recommendations
- Confidence level

### Passes To
- **x-writing**: If recommendation involves content format decisions
- **(none)**: Usually terminal skill (answers question directly)

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Citing old "reply = 13.5x" as official | Check xai-org/x-algorithm for current docs |
| Confusing inference with documentation | Label community observations clearly |
| Not checking for recent changes | Always check last 7 days for commits/announcements |
| Overgeneralizing from single data point | Look for patterns across multiple sources |
| Ignoring topic clustering | Authority is topic-specific, not global |

## Token Optimization

**Do NOT load this skill unless:**
- Question is specifically about X algorithm, ranking, or distribution
- Content format decision requires algorithm knowledge
- User asks about engagement optimization

**If question is about:**
- Market research → Use market-research
- Claim validation → Use source-verification
- Narrative positioning → Use narrative-analysis
- Writing style → Use x-writing + writing-style.md

---

*Skill version: 2.0 | Last updated: 2026-09-05*
