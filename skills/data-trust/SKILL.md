---
name: data-trust
description: Decide whether a marketing number is good enough to make a decision on, before making it. Audits tracking coverage, source taxonomy, deduplication and platform-versus-record gaps. Use before any budget reallocation or channel comparison.
---

# Data trust

The most useful sentence this skill can produce is *"these numbers are not
decision-grade."* Say it when it is true.

## The four failures, in order of frequency

**1. Taxonomy gaps.** The source field has no value for organic, direct or
referral, so those conversions fall into whatever the form defaults to — usually
the paid bucket. **This flatters paid and starves organic**, and it is by far
the most common failure.

Audit: list every distinct value in the source field with its share. If organic,
direct and referral are absent or implausibly small, every channel number
downstream is wrong.

**2. Missing tags.** Measure the share of sessions or leads arriving with no UTM
at all. Above roughly 10-15% and channel splits are indicative, not decisive.

**3. Double counting.** Two platforms claiming the same conversion, or a pixel
firing twice. Symptom: platform-reported conversions summed across channels
exceed what the business actually recorded. Deduplicate on an order or
transaction id, never on a session.

**4. Value corruption.** Counts reconcile, revenue does not — usually a pixel
sending a static value on every event. Check both, separately.

## Reconcile against something the platform does not control

Ad platforms are graded by their own homework. Pick a source of truth
deliberately — the payment processor, the CRM, or the operational record the
business actually runs on — then compare, for the same window and definition:

| | |
|---|---|
| Under 10% gap | Normal. Attribution windows and restatement explain it |
| 10-25% | Investigate before reallocating |
| Over 25% | One of the two is wrong. Find out which before anyone moves budget |

## Traps

- **Referrer is not channel.** Traffic arriving from a social domain is often a
  *paid* placement on that platform. Only the UTM medium separates organic
  social from paid social. Diagnosing "organic is working" from referrer alone
  is a common and expensive error
- **Compare like windows.** 7-day-click and 1-day-click answer different
  questions. Pick one and hold it
- **Yesterday is provisional.** Attribution restates for days
- **Absence of a source value is not absence of the channel.** It usually means
  nobody added it to the form

## Output

The taxonomy audit as a table of values and shares. The untagged share. The
platform-versus-record gap per channel with a verdict. Then one line: are these
numbers safe to decide on, and if not, the single fix that would make them so.
