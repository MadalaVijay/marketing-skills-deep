---
name: pricing-decisions
description: Reason about price level, tier structure and discounting without guessing. Covers what a price test can and cannot tell you, willingness-to-pay research, and why discounting usually costs more than it earns. Use when setting or changing price, designing tiers, or evaluating a discount.
---

# Pricing decisions

Price is the fastest lever on profit and the one most often set by feel. It is
also the hardest thing to A/B test honestly.

## Why price tests are different

You usually cannot run a clean price test:

- **Charging different customers different prices** for the same thing creates
  fairness and, in some markets, legal exposure
- **The effect is slow.** Price changes churn and expansion for months. A
  two-week test measures signup rate, which is not the thing you care about
- **Signup rate is the wrong metric anyway.** A higher price with fewer signups
  can be strictly better. Judge on **contribution margin per visitor**, not
  conversion

Where a test is possible, run it on **new cohorts only**, hold existing
customers harmless, and commit up front to measuring for a full retention cycle.

## When you cannot test, do this instead

- **Van Westendorp** four questions (too cheap / cheap / expensive / too
  expensive) gives an acceptable range from a modest sample. Directional, not
  precise
- **Compare against the category anchor, not against cost.** Buyers price you
  against the nearest familiar alternative. If the category trains people to
  expect a low entry price, being several times it needs a visible reason
- **Watch what people already pay** for the adjacent thing they use today
- **Sell the duration, not just the tier**, where the purchase is recurring.
  Longer commitments often price better than deeper discounts

## Tier design

- **Three tiers works** because it gives a reference point, not because three is
  magic. The middle tier is chosen most often when the top exists
- **Differentiate on a dimension the buyer can predict for themselves** — seats,
  volume, frequency. Feature-gating on things buyers cannot forecast produces
  wrong-tier purchases and churn
- **Do not let the cheapest tier be good enough** for the core use case, or the
  ladder never lifts
- **Check the payment ceiling.** Many markets have mandate or auto-debit limits
  above which recurring payment silently fails or requires re-authentication.
  A price just over that ceiling can look fine and quietly break renewals

## Discounting

Model it before you approve it. A 20% discount on a 40% contribution margin
removes **half** the margin, so it needs to double volume just to break even.
State that arithmetic explicitly whenever a discount is proposed.

Worse, discounts train the buyer. A brand that discounts predictably teaches
people to wait, which shifts full-price demand into the discount window and
looks like the discount worked.

Prefer, in order: longer commitment, bundled value, then price cuts last.

## When to refuse

- Contribution margin unknown. Ask first
- Asked to project revenue from a price change with no retention data
- Asked to justify a price already decided. Say what the evidence supports

## Output

The recommendation, the evidence class behind it (test, research, or judgement),
what it would take to be wrong, and the one metric to watch after the change.
For a discount: the break-even volume lift, stated as arithmetic.
