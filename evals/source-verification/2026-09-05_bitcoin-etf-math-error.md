# Negative Verification Case - Bitcoin ETF Swing Math

## Trigger

A draft claimed:

> "IBIT swung $407M in one session. From -$201M to +$454M."

## What Was Wrong

- The arithmetic was wrong.
- The time interval was wrong.

## Correct Calculation

```text
Sep 1: IBIT -$201M
Sep 3: IBIT +$454M

Directional swing = $454M - (-$201M) = $655M
Interval = two trading days, not one session
```

## Publication-Safe Wording

> "IBIT moved from about -$201M on Sep 1 to +$454M on Sep 3 - a $655M directional swing over two trading days."

## Lesson

1. Recalculate all derived numbers.
2. Preserve signed values in the formula.
3. State the actual time interval.
4. A correct underlying data point can still become a false claim through bad arithmetic.

## Verification Rule Added

No draft may use a derived number without a visible calculation in the claim ledger.

---

*Date: 2026-09-05*