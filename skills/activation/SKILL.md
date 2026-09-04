---
name: activation
description: Find the moment that predicts retention and get more people to it. Covers identifying the activation event from data rather than intuition, time-to-value, and why most onboarding work targets the wrong step. Use when new users do not stick, or before redesigning onboarding.
---

# Activation

Activation is the earliest observable behaviour that predicts long-term
retention. It is found in data, not chosen in a workshop.

## Finding it, not guessing it

The common failure is picking a plausible-sounding milestone — "completed
profile", "invited a teammate" — and optimising for it. Plausible milestones
correlate with retention because engaged people do everything, not because that
step causes anything.

Method:

1. Take cohorts old enough to have observed retention
2. For each candidate early action, split users into did and did not
3. Compare retention at a fixed later point
4. The candidate with the **largest separation** and **enough volume on both
   sides** is your activation event

**Then check causality is plausible.** If the action is something only already
committed users would do, you have found a symptom. The useful activation event
is one you can *cause* through design.

## Time to value matters as much as the event

The same event reached on day 1 predicts far better than reached on day 20. Track
both **whether** and **how quickly**. Shortening time-to-value is often easier
than raising completion, and pays more.

## Where onboarding work usually goes wrong

- **Optimising the step with the biggest drop.** Signup-to-first-action always
  has the largest drop. It is also where the least committed people leave, and
  many of them should
- **Adding education instead of removing steps.** A tour explains a form that
  should be shorter. Removing a field beats explaining it
- **Front-loading setup.** Anything asked before value is delivered is a tax on
  people who do not yet know if they want it. Defer everything you can
- **One path for everyone.** Users arrive with different intent; a single linear
  onboarding serves the median and loses the tails

## The counter-check

Higher activation with **lower** retention among activated users means the
funnel is pushing people through a milestone without delivering the value it
represents. Always report both together.

## When to refuse

- No cohort has enough history to observe retention. State how long is needed
- Fewer than ~200 users per arm of the comparison
- Asked to validate a pre-chosen activation metric. Test it against the data
  and say what the data supports

## Output

The candidate activation events ranked by retention separation, with volume on
each side. The recommended definition, why it is plausibly causal rather than
correlated, current completion rate and median time to reach it, and one change
aimed at the largest addressable drop before that moment.
