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

**5. Counting rows instead of events.** Operational logs are usually
append-only: a record is written every time something is touched, so one
underlying event appears as many rows. Row count then overstates reality by
whatever the average touch count happens to be, and the multiple is not stable
over time.

**Never report a row count from an operational log as an event count.** Count
distinct keys — the order, the customer, the date, whichever identifies the
thing once — and state which key you used. If no such key exists, that is the
finding.

The same trap in calendar form: counting filled cells rather than distinct
periods. A schedule with one row per participant per occurrence counts an
occurrence once per participant, not once.

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
- **Two events with similar names are not the same event.** A generic
  `Lead` and a product-qualified `Product Lead` measure different populations,
  and merging them to tidy a report destroys the only distinction that made
  either useful. Before combining any two events, confirm they fire from the
  same trigger on the same population — not merely that the names look alike
- **A field name that changes breaks every downstream parser silently.** An
  integration that labels a value `Phone:` and later `Phone Number:` will keep
  delivering data while anything matching the old label quietly reads empty.
  When a series drops to zero without a business explanation, check the field
  names before checking the market
- **Absence of a source value is not absence of the channel.** It usually means
  nobody added it to the form

## Output

The taxonomy audit as a table of values and shares. The untagged share. The
platform-versus-record gap per channel with a verdict. Then one line: are these
numbers safe to decide on, and if not, the single fix that would make them so.

See also `form-friction`, which depends on this skill's verdict before any
completion rate can be believed.
