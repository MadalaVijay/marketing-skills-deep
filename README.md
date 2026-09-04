# marketing-skills-deep

Marketing skills for AI agents, built for depth over coverage.

There are good broad libraries already. [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)
has 50 skills spanning copywriting, SEO, popups, PR and more, and if you want
breadth you should use it.

This is the other half. Ten skills, each long, for the questions where a
shallow answer is worse than none:

**Is this number true? Is this channel actually profitable? Is that result real
or noise? Where is the funnel really leaking?**

```
skills/
  funnel-diagnosis/     where the funnel leaks, and where it only appears to
  unit-economics/       whether a channel makes money, at the margin
  data-trust/           whether a number is decision-grade before you act on it
  experiment-design/    sample size, significance, when to stop looking
  pricing-decisions/    tiers, price tests, and discount discipline
  retention-diagnosis/  reading cohorts without fooling yourself
  activation/           time to value, and the one moment that predicts retention
  channel-fit/          which channel suits which business, and when to quit one
  capacity-economics/   when the profit lever is occupancy, not price
  form-friction/        where the form loses people you already paid for
```

## Install

```bash
git clone https://github.com/MadalaVijay/marketing-skills-deep
cp -r marketing-skills-deep/skills/* your-project/.claude/skills/
```

## What makes these different

**They refuse.** Every skill states the conditions under which it will not give
an answer. Below roughly 30 conversions, most differences you can see are noise,
and a skill that produces a confident verdict anyway is worse than no skill.

**They separate marginal from average.** A channel at 3x blended return can be
losing money on its most recent spend. Almost every marketing mistake at scale
lives in that gap.

**They check the instrument before the reading.** A conversion event that
stopped firing looks identical to traffic that stopped converting, and it is far
more common. Several of these skills check the tracking before they diagnose
the marketing.

**They are opinionated, and say which opinions are conventions.** Where a
threshold is a rule of thumb rather than arithmetic, it says so and tells you to
tune it.

**They cover constraints that spreadsheets miss.** The ceiling your recurring
payment method puts on your own pricing. The margin that only exists because
customers do not consume what they bought. The operational log whose row count
is several times its event count. These decide real outcomes and are almost
never written down.

## What is not here

No copywriting, no creative generation, no SEO audits, no outreach sequences.
Those are execution, they are well covered elsewhere, and an LLM is already
good at them. These are the judgement calls that sit above execution.

No automation, no API writes, no bid management. These read and advise.

## Companion repos

- [paid-ads-skills](https://github.com/MadalaVijay/paid-ads-skills) — the same
  approach applied to running paid media day to day

MIT licensed.
