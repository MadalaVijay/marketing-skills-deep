---
name: experiment-design
description: Design a marketing test that can actually answer the question, and read the result honestly. Covers sample size, run length, stopping rules and the difference between a real effect and noise. Use before launching a test, or when asked whether a result is real.
---

# Experiment design

Most marketing tests cannot detect the effect they are looking for. They run,
produce a number, and the number gets believed.

## Before the test: can it possibly answer?

Ask for the **minimum effect worth acting on**, not the effect you hope for. If
a 5% lift would not change any decision, do not power the test for 5%.

Rough sample size for a conversion test, per variant:

```
n ≈ 16 × p × (1 − p) / (minimum detectable effect)²
```

where `p` is the current conversion rate as a decimal and the effect is absolute.
Going from 2% to 2.4% is an absolute effect of 0.004, and needs roughly 300,000
per variant. Most teams discover this and quietly test for 50% lifts instead.

Report the number honestly. **If the traffic does not exist, say the test cannot
be run** and suggest a different question: a bigger change, a higher-traffic
surface, or a qualitative method.

## Run length

- **Full weeks only.** Weekday and weekend behaviour differ in nearly every
  consumer category. A test stopped on a Wednesday is a test of Wednesdays
- **Minimum two weeks** for anything with a purchase cycle
- **Long enough to cover the conversion lag.** If people convert 8 days after
  first touch, a 7-day test measures the wrong thing

## Stopping rules, set in advance

**Peeking is the most common way marketing tests lie.** Checking daily and
stopping when it looks significant produces false positives at several times the
stated rate, because you get many chances to cross the line by chance.

Set the sample size and the end date before launch. Then look at the end.

If you must monitor, monitor for **harm** — a variant losing badly enough to be
worth killing — not for wins.

## Reading the result

- **Under ~30 conversions per variant, do not call it.** Say the test is
  inconclusive
- **A non-significant result is not "no difference."** It means the test could
  not detect one. Report the range the true effect could plausibly sit in
- **Check the segments only to generate hypotheses, never to rescue a null.**
  Slicing until something is significant will always eventually succeed
- **Confirm the split was actually even** and that both variants were served
  through the same period

## What not to test

Small copy changes on low-traffic pages. The effect is too small and the
traffic too thin, ever. Change something big enough to matter, or research it
qualitatively instead.

## Output

For a planned test: required sample per variant, expected run length at current
traffic, the pre-registered stopping rule, and a plain statement of whether the
test is feasible. For a completed test: the verdict, the plausible effect range,
and whether the design permits the conclusion being drawn.
