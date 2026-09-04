---
name: retention-diagnosis
description: Read retention and churn honestly using cohorts, separating a genuine retention problem from a mix-shift, a measurement artefact, or an acquisition problem wearing retention clothes. Use when churn rises, before building winback, or when asked why retention is falling.
---

# Retention diagnosis

Most retention problems are acquisition problems that surface later.

## Always cohort. Never look at aggregate churn.

Aggregate churn moves when the **mix** changes, with no change in behaviour. Grow
acquisition quickly and aggregate churn rises simply because new customers churn
faster than tenured ones. The business improved; the metric worsened.

Split by **signup month**, then read down each cohort. That is the only view
where a real change is visible.

## The question to ask first

**Did the customer ever get value?** Retention curves usually break in the first
period, not gradually. A cohort that drops 60% in month one and then flattens
does not have a retention problem, it has an activation problem, and winback
campaigns aimed at those people will not work.

Look for where the curve **flattens**. If it flattens, the business has a stable
core and the issue is getting people to it. If it never flattens, the product is
leaking indefinitely and no amount of lifecycle marketing fixes that.

## Separate the four causes

| Symptom in cohorts | Likely cause |
|---|---|
| Recent cohorts worse from month one, older ones stable | **Acquisition quality** changed. Check channel mix and targeting first |
| All cohorts worsen at the same calendar point | Something **happened**: a price change, an outage, a policy change, a competitor |
| Curve declines steadily and never flattens | **Product value** does not sustain. Not a marketing problem |
| Only one segment worsens | Mix shift. The average is hiding two populations |

The first row is the most common and the most misdiagnosed. A channel that
delivers cheap signups who never activate shows up as a retention problem three
months later, and the retention team gets asked to fix it.

## Measurement traps

- **Define churn before measuring it.** Cancellation, failed payment, and
  non-usage are three different events. Involuntary churn from expired cards is
  often a large share and is a payments problem, not a marketing one
- **A renewal not yet due is not a retention.** Only count customers who reached
  the decision
- **Paused is not churned**, but do not let it hide churn either. Track it
  separately and check whether paused customers return
- **Survivorship.** Reading only surviving customers' satisfaction tells you
  about survivors

## Before recommending winback

Winback works on people who got value and left for a reason. It does not work on
people who never activated. Segment by whether the customer reached the value
moment before spending anything on reactivation.

## When to refuse

- Cohorts too young to show a curve. Say how long is needed
- Fewer than ~50 customers per cohort
- Churn definition unstated

## Output

The cohort table, where the curve flattens, which of the four causes fits with
evidence, and one intervention aimed at the actual cause. Say plainly if the
diagnosis is that marketing cannot fix it.
