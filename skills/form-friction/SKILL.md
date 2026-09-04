---
name: form-friction
description: Find where a lead form or checkout loses people, and size the loss against the cost of the traffic feeding it. Distinguishes a form problem from a traffic problem before anyone rewrites copy. Use when conversion is below expectation, or before increasing spend on a page that already receives traffic.
---

# Form friction

The most expensive conversion problem is usually not the headline, the offer, or
the audience. It is that a meaningful share of people who *decided to convert*
and started filling something in did not finish.

Those people are the cheapest customers you will ever get, because you have
already paid for them.

## Size it before diagnosing it

Ask for three numbers:

- **starts** — people who interacted with the first field
- **completions** — people who submitted
- **cost of the traffic** that produced the starts

Then:

```
completion rate = completions / starts
abandons        = starts − completions
implied waste   = abandons × cost per start
```

`implied waste` is the number that gets a form fixed. A completion rate in the
20-30% range on a short form usually means something is broken, not that
visitors were unserious — but treat that band as a prompt to investigate, not a
diagnosis, because acceptable rates vary enormously by form length, price point
and how qualified the traffic is.

**If starts are not instrumented, that is the first finding.** Submit-only
tracking cannot distinguish a form nobody reached from a form everybody
abandoned, and those have opposite fixes.

## Separate the form problem from the traffic problem

| Pattern | Reading |
|---|---|
| Many starts, few completions | Form problem. Fix the form |
| Few starts relative to sessions | Page or offer problem. The form is innocent |
| Completions fine, sales poor | Neither. Look downstream at qualification or follow-up |

Running a copy test on a page whose form is the constraint wastes the test.
Establish which of the three you are in before recommending anything.

## Where forms actually lose people

Ordered by how often it turns out to be the cause:

1. **Fields that are not needed to make the sale.** Every field is a chance to
   stop. Ask what breaks if it is removed, and remove it if nothing does. The
   sales team wanting it is not the same as the sale needing it
2. **Mobile input mismatch.** A numeric field that summons a full keyboard, a
   date picker that fights the OS, a submit button under the keyboard. Where
   most traffic is mobile this dominates everything else, so check the mobile
   completion rate separately — a healthy blended rate can hide a broken one
3. **Validation that punishes.** Errors shown only on submit, a cleared form
   after a failure, a phone format rejected without explanation
4. **Silent failure.** Submissions that never arrive, or a success screen that
   fires while the write fails. Test the full path end to end with a real
   submission and confirm it reached the system of record
5. **Trust asked for too early.** Payment or identity details before the value
   is clear
6. **Unexplained cost.** A price, fee or commitment first revealed at the last
   step

## Mobile is a separate funnel

Report completion by device always. They are different products with different
failure modes, and the fix for one frequently does nothing for the other.

## Verify the instrument before believing the number

A collapsed completion rate is as likely to be a tracking change as a behaviour
change. Before diagnosing, confirm the start and completion events still fire,
still fire once, and that two similarly-named events have not been merged into
one. See `data-trust`.

## When to refuse

- Starts are not tracked, so abandonment cannot be separated from non-arrival
- Fewer than ~100 starts in the window — completion rates on small samples swing
  wildly
- The tracking changed inside the comparison window
- Device split unavailable and most traffic is mobile

## Output

Starts, completions, completion rate overall and by device, abandons, and
implied waste in currency. Then the single most likely cause from the ordered
list with the evidence for it. Then the one change to make first, and what you
expect it to recover — stated as a range, not a point estimate.
