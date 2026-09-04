---
name: funnel-diagnosis
description: Find where a funnel actually leaks, separating real drop-off from measurement artefacts and from steps that only look bad. Use when conversion is falling, when asked "where should we focus", or before committing budget to fixing a stage.
---

# Funnel diagnosis

Most funnel work fixes the stage with the worst-looking number. That is usually
the wrong stage.

## Order of operations

**1. Check the instrument before the reading.**
A step that reports 3% conversion may be converting at 30% and firing its event
once in ten times. Before diagnosing anything, confirm each step's event is
recording — compare against a source the front end does not control, such as the
database, the CRM or the payment processor. A conversion event that silently
stopped looks exactly like a funnel that stopped converting, and it is far more
common.

**2. Size the leak in absolute terms, not percentages.**
A step converting at 20% that 500 people reach loses 400 people. A step
converting at 60% that 20,000 people reach loses 8,000. Fix the second one. The
first has the uglier number and a twentieth of the upside.

**3. Compare each step to its own history, not to a benchmark.**
Published funnel benchmarks are close to useless: they average across price
points, categories, traffic sources and intent. A step is underperforming when
it is worse than it was, or worse than the same step for a comparable segment
in your own data.

## Where the leak usually is not

- **The step with the lowest conversion rate.** Some steps are meant to be
  narrow. A checkout that converts 40% of carts is not broken; a homepage that
  sends 4% to product is doing its job.
- **The last step before the drop.** People abandon at checkout for reasons
  formed three steps earlier: unclear pricing, missing trust, wrong expectation.
  The visible abandon is often a lagging symptom.
- **The stage everyone argues about.** Attention concentrates on the stage with
  an owner, not the stage with the loss.

## Segment before concluding

An overall funnel number is a weighted average of very different behaviours.
Before diagnosing, split by at least:

- **Traffic source.** Paid, organic and direct convert differently at every step
- **Device.** Mobile form completion is routinely half of desktop
- **New versus returning**
- **Intent tier**, where you can infer it — branded search behaves nothing like
  a cold interest audience

A funnel that looks mediocre in aggregate is often two funnels: one healthy, one
broken. Fixing the average fixes neither.

## Quantify before recommending

For each candidate leak, state: people lost per month, the conversion lift you
would need to matter, and whether that lift is plausible. "Improve checkout by
30%" is not a plan. "Recover 400 of the 615 monthly form abandons by cutting
three fields" is.

## When to refuse

- Fewer than ~100 people through the step in the window. Rates on small numbers
  swing wildly
- Event integrity unverified. Say so and stop
- No segmentation available. Give a provisional read and label it provisional

## Output

The three largest leaks by absolute loss, each with the count, the segment it
concentrates in, the evidence the tracking is sound, and one specific change
with an estimated recovery. Then explicitly: which stage looks worst but is not
worth fixing, and why.
