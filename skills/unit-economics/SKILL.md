---
name: unit-economics
description: Work out whether a channel or cohort actually makes money, separating marginal from blended economics and accounting for payback. Use before scaling spend, when comparing channels, or when a profitable-looking channel is not producing cash.
---

# Unit economics

The question is never "what is our ROAS". It is "does the next unit of spend
make money, and can we survive the wait".

## Four numbers, and the order they matter

**1. Contribution margin per customer**, not revenue. Revenue minus COGS,
payment fees, shipping, support and any per-unit variable cost. Marketing
against revenue overstates every channel, and by more in low-margin businesses.

**2. Marginal CAC**, not blended. Blended CAC averages your cheapest historical
customers with your most recent ones. Approximate the margin:

```
marginal CAC ≈ (spend_recent − spend_prior) / (customers_recent − customers_prior)
```

using two adjacent equal-length windows. It is crude and seasonality-sensitive.
Say so. It still answers the question blended CAC does not.

**3. Payback period.** How many months of contribution margin to recover CAC. A
business with three months of runway cannot fund a nine-month payback at any
return multiple. This kills more companies than bad ROAS does.

**4. Retention-adjusted LTV.** Only after the above. LTV built on an optimistic
retention curve is the most common way a bad channel looks good.

## The trap

A channel at 3x blended return can be losing money on its most recent spend
while the average still looks healthy, because early cheap conversions drag it
down. You scale, the average worsens, and the scale-up gets blamed. It was
already unprofitable at the margin before you touched it.

**Always compute both, and lead with the marginal number.**

## LTV honesty

- **Use realised retention where you have it.** A cohort with three months of
  history gives you three months of LTV, not a projection to 24
- **State the retention assumption explicitly** whenever you project
- **Cap the horizon at something the business can finance.** LTV over 36 months
  is irrelevant to a company that needs cash in six
- **Segment it.** LTV averaged across a whale and a churner describes neither

## Ratios, and their limits

`LTV:CAC of 3:1` is a convention, not a law, and it is silent on timing. Two
businesses with identical 3:1 ratios and payback of 2 months versus 14 months
are in completely different situations. Report the ratio **and** the payback, or
the ratio misleads.

## When to refuse

- Contribution margin unknown. Ask; do not substitute revenue
- Fewer than ~30 conversions in the window
- Cohorts too young to observe retention, and a projection would carry the answer
- Attribution not verified — see the `data-trust` skill first
- **Delivery cost is per slot rather than per customer.** Where a class, van,
  appointment or route costs roughly the same however many customers it serves,
  per-customer margin is a function of occupancy and this skill will understate
  the real lever. Use `capacity-economics` instead

## Output

Contribution margin per customer, blended CAC, marginal CAC, payback in months,
and the retention assumption stated in words. Then a verdict: scale, hold, or
stop, with the single number that would change it.
